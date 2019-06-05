# Jets Project

Test Project to debug hot reloading in development for issue Reloading all folders inside app: https://github.com/tongueroo/jets/issues/280

## Usage

Install:

    git clone https://github.com/tongueroo/demo-reload
    bundle

Start server:

    jets server

Curl the posts endpoint:

    curl localhost:8888/posts

Change files:

* [app/serializers/post_serializer.rb](app/serializers/post_serializer.rb)
* [app/services/post_service.rb](app/services/post_service.rb)

Curl the posts endpoint again and see the changes:

    curl localhost:8888/posts

## Example

Before:

    $ curl localhost:8888/posts ; echo
    {"serialize":{"title":"test1editanother"},"service":"list3"}
    $

After:

    $ curl localhost:8888/posts ; echo
    {"serialize":{"title":"test1editanother","body":null},"service":"list1"}
    $