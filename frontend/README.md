# React Frontend
## Project Setup
Set development environment variables:
```
source api/bin/dev.sh
```
Start the backend API server:
```
yarn start-api
```
Load `test_db` into your local database `shiba_nearby`:
```
gunzip < test_db.gz | mysql shiba_nearby -u root -p
```
> Note: this will replace your local database, but it shouldn't matter at this point. More on setting up and using a
> local MySQL database: [click here](../backend/README.md#setting-up-mysql-database)

## yarn
The command `yarn check` has been historically buggy and under-maintained. Please use the following commands instead.
```
yarn check --integrity
```
> Verifies that versions and hashed values of the package contents in the project’s package.json match those in yarn
>'s lock file. This helps to verify that the package dependencies have not been altered.
```
yarn check --verify-tree
```
> Recursively verifies that the dependencies in package.json are present in node_modules and have the right version
>. This check does not consider yarn.lock.

## Miscellaneous
[UI mockup](https://rp.mockplus.com/run/Bz-NJt4jwK/bT0eRYaJfM?cps=expand&rps=expand&nav=1&ha=1&la=1&fc=0&out=0&rt=1&moduleID=zZaWOQ4d4OMZ&appID=FW1Q6W1BVULe)
