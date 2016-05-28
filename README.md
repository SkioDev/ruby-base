# ruby-base
Dockerfile for ruby base image


## How to update
To update to version X.X.X:
- Change the RUBY_VERSION environment variable in the Dockerfile to X.X.X
- Change the RUBY_BASE_VERSION environment variable in the Dockerfile to X.X
- Visit https://www.ruby-lang.org/en/downloads/ to get the sha256 hash for the
  version you are trying to build and update the RUBY_SHA256 environment
  variable in the Dockerfile to that value
- Run `docker build -t skio/ruby .` and make sure that the image builds
- Make sure you're on the master branch and run
  `git commit -m "Update to Ruby version X.X.X"
- Run `git push -u` to update the latest tag
- Create a new branch `git checkout -b X.X.X`
- Run `git push -u` to add the version tag