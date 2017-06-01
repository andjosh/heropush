heropush
===

This is a simple `bash` script to create a [Heroku][0] application build/deploy from a directory. It uses Heroku's new V3 API, created to replace tools like [`dpl`][2].

## Usage
~~~sh
./heropush ~/some_dir
# or from within
./heropush .
# specifying app on the fly
HEROKU_APP=foobar ~/heropush ~/some_dir/foobaz
~~~

The script requires two `ENV` variables - `HEROKU_APP` and `HEROKU_API_KEY`. You can grab a Heroku API key [on your account page][1].

## Installation
~~~sh
curl -L https://github.com/andjosh/heropush/blob/master/heropush
chmod +x heropush
~~~

The script has no external dependencies aside from what should already be on your *nix machine (grep/curl/awk/sed/cut)

## Sample CI/CD script
~~~sh
curl -L https://github.com/andjosh/heropush/blob/master/heropush && chmod +x heropush && ./heropush .
~~~

[0]: https://heroku.com
[1]: https://dashboard.heroku.com/account
[2]: https://github.com/travis-ci/dpl