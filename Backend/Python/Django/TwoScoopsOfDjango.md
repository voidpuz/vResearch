# Two Scoops of Django 3x

My conslusions on reading the book, usages of best-practices and possible problems to avoid.

### Chapter 1: Coding Style

**Readability**. What this means is that you should go the extra mile to make your code as readable as possible:
- Avoid abbreviating variable names.
- Write out your function argument names.
- Document your classes and methods.
- Comment your code.
- Refactor repeated lines of code into reusable functions or methods.
- Keep functions and methods short. A good rule of thumb is that scrolling should not be necessary to read an entire function or method.

**PEP 8**. Use pre-commit and `ruff` linter's default configurations to follow common PEP8 rules, such as:
- 79 character length
- no star imports
- group imports by: standard-library, third-party, local
- prefer absolute imports over relative
- use underscores in URL patterns over dashes
- don't call functions or evaluate expressions inside of string interpolation:

```python
# Allowed
f"hello {user}"
f"hello {user.name}"
f"hello {self.user.name}"

# Disallowed
f"hello {get_user()}"
f"you are {user.age * 365.25} days old"

# Allowed with local variable assignment
user = get_user()
f"hello {user}"
user_days_old = user.age * 365.25
f"you are {user_days_old} days old"
```

- Follow other guides shown [here](https://docs.djangoproject.com/en/5.2/internals/contributing/writing-code/coding-style/)
- Follow [PEP257](https://peps.python.org/pep-0257/) for docstrings


### Chapter 2: The Optimal Django Setup

1. Don't use SQLite in production. It is treated as a file and does not support concurrency as postgres or similar database servers support.
2. Use a modern, production-ready package managers, such as `uv`.
3. Prefer `Docker` or similar containerization tool over raw systemd service.


### Chapter 3: How to Layout Django Projects

1. Use a cookiecutter or build your own boilerplate.


### Chapter 4: Django App Design

1. Each app should be tightly focused on its task.
2. Common app modules:

```
# Common modules
app1/
├── __init__.py
├── admin.py
├── forms.py
├── management/
├── migrations/
├── models.py
├── templatetags/
├── tests/
├── urls.py
├── views.py
```

3. Uncommon app modules:

```
# uncommon modules
app1/
├── behaviors.py
├── constants.py
├── context_processors.py
├── decorators.py
├── db/
├── exceptions.py
├── fields.py
├── factories.py
├── managers.py
├── middleware.py
├── schema.py
├── signals.py
├── utils.py
├── viewmixins.py
```
The purpose of these files are:
- `behaviors.py` - An option for locating model mixins;
- `constants.py` - A good name for placement of app-level settings;
- `decorators.py` - Where we like to locate our decorators;
- `db/` - A package used in many projects for any custom model fields or components;
- `fields.py` - is commonly used for form fields but is sometimes used for model fields when there isn’t enough field code to justify creating a `db/` package;
- `factories.py` - Where we like to place our test data factories;
- `managers.py` - When `models.py` grows too large, a common remedy is to move any custom model managers to this module;
- `schema.py` This is where code behind GraphQL APIs is typically placed;
- `signals.py` - While we argue against providing custom signals, this can be a useful place to put them;
- `utils.py` - utility functions;
- `viewmixins.py` - View modules and packages can be thinned by moving any view mixins to this module.

4. Alternatively, we can use **service layer** approach (I personally prefer independent functions to perform business logic, as they are testable and reusable).


### Chapter 5: Settings and Requirements Files

Some best practices to follow:
- **All settings files need to be version-controlled.** This is especially true in production environments, where dates, times, and explanations for settings changes absolutely must be tracked.
- **Don’t Repeat Yourself.** You should inherit from a base settings file rather than cutting-and-pasting from one file to another.
- **Keep secret keys safe.** They should be kept out of version control.

**Using Multiple Settings Files.** Instead of having one `settings.py` file, with this setup you have a `settings/` directory containing your settings files. This directory will typically contain something like the following:
```
settings/
├── __init__.py
├── base.py
├── local.py
├── staging.py
├── test.py
├── production.py
```
Configure `DJANGO_SETTINGS_MODULE` to declare which settings file to use.

**Using Environment Variables Pattern.** Every operating system supported by Django (and Python) provides the easy capability to create environment variables. PLEASE use them. Everything - API keys, secret keys, credentials, etc - should be stored in environment variables.

