# heroku-buildpack-s3-asset-sync

This buildpack allows uploading a local directory to an S3 bucket during slug
compilation.

It is based on the [AWS CLI buildpack](https://github.com/heroku/heroku-buildpack-awscli).

## Usage

Example usage:

    $ heroku buildpacks:add https://github.com/viewthespace/heroku-buildpack-s3-asset-sync.git

    $ heroku config:add ASSETS_AWS_ACCESS_KEY_ID=<aws-access-key>
    $ heroku config:add ASSETS_AWS_SECRET_ACCESS_KEY=<aws-secret-access-key>
    $ heroku config:add ASSETS_AWS_S3_BUCKET=my-bucket
    $ heroku config:add ASSETS_LOCAL_PATH=public/
