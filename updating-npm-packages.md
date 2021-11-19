# Updating/Installing npm packages

When installing/updating an npm package, make sure to clean the entire build and install everything again, i.e., run `make clean` followed by `make dev`, or run `make development-build`.

This is because whenever we're editing packages in the environment the only way we've found to test them is to clean the entire build and rebuild everything to re-install everything the way it would be installed in the server.
