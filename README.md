# saythanks

A Clojure library designed to thank people who wish you on Facebook on
your birthday.

## Pre-requisites

You need to install Redis in order to use this code. We need Redis to
store the point to which we've replied to posts. This allows us keep
continuously polling Facebook and reply to everyone who wishes us.

## Usage

1. Create the file src/saythankyou/access.clj

Add the following code to it:

    (ns saythanks.access)
    (def access-token "<your access token>")

Add your access token here.
Get it from https://developers.facebook.com/tools/explorer
you need to give the read_stream and publish_stream permissions.

2. Change the default thank-you messages in src/saythanks/core.clj

(If you wish, I think the defaults are quite good.)
A thank-you message will be picked at random and used to reply to the
facebook post.

3. Go to the terminal and run:

    $ lein uberjar
    $ java -jar ./target/saythanks-0.1.0-SNAPSHOT-standalone.jar

Enjoy :)

## License

Copyright © 2012 Vedang Manerikar

Distributed under the Eclipse Public License, the same as Clojure.
