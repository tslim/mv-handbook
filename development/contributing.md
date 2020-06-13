# Contributing

As a contributor, here are the guidelines we would like you to follow:

 - [Commit Message Guidelines](#commit)

## <a name="commit"></a> Commit Message Guidelines



### Commit Message Format
Each commit message consists of a **type**, a **scope** and a **subject**:

```
<type>(<scope>): <subject>
```

The **type** is mandatory and the **scope** is optional.

Samples:

```
docs(changelog): update changelog to beta.5
```
```
fix(release): need to depend on latest rxjs and zone.js
```

### Type
Must be one of the following:

* **build**: Changes that affect the build system or external dependencies
* **ci**: Changes to our CI configuration files and scripts (example scopes: Circle, BrowserStack, SauceLabs)
* **docs**: Documentation only changes
* **feat**: A new feature
* **fix**: A bug fix
* **perf**: A code change that improves performance
* **refactor**: A code change that neither fixes a bug nor adds a feature
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
* **test**: Adding missing tests or correcting existing tests

### Scope
The scope should be the name of the app under the umbrella project.

The following is the list of supported scopes:

* **academy**
* **academy_web**
* **analytics**
* **api**
* **asset_progress**
* **event_stream**
* **feature_toggle**
* **migrator**
* **mindvalley_com**
* **services**
* **spaces**

### Subject
The subject contains a succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize the first letter
* no dot (.) at the end
