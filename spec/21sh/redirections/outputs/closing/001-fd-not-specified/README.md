# 001-fd-not-specified

*[spec > 21sh > redirections > outputs > closing](..) > 001-fd-not-specified*

### Shell commands that are sent to the standard entry

```bash
/bin/ls .. invalid_folder >&-

```

### What is expected on standard output

```bash
expected_to_not have_regexp "42shTests.sh"

```

### What is expected on error output

```bash
expected_to_not be_empty
might have_regexp "[Nn]o such file or directory"

```

### Variables

The following variables may appear in the tests:

* ${**GLOBAL_INSTALLDIR**} -> The installation directory of 42shTests
* ${**GLOBAL_TMP_DIRECTORY**} -> The temporary directory in which tests are executed
* ${**GLOBAL_TOKEN**} -> A token that changes value at launch time
* ${**PATH**} -> The standard environment variable PATH
* ${**HOME**} -> The standard environment variable HOME