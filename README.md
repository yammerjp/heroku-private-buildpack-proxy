Use a heroku buildpack on private repository

## Usage

```
heroku config:set --app=foo PRIVATE_BUILDPACK_KEY="-----BEGIN OPENSSH PRIVATE KEY-----\nxxxxxxxxxxxxxxxxxx-deploy-key-of-your-private-repository-xxxxxxxxxxxxx\nxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx\nxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx\nxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx\n-----END OPENSSH PRIVATE KEY-----\n"
heroku config:set --app=foo PRIVATE_BUILDPACK_REPO=git@github.com:your-account/your-private-repository.git
heroku buildpacks:add --app=foo  https://github.com/yammerjp/heroku-private-buildpack-proxy.git
```
