#Usage

###Starting the server

    cd $ROOTDIR
    go build
    ./<executable>

You should be able to query the API at localhost:3000/user/. You will need a authorization key to
interact with the API and that is under the header "Authorization: secret".

###Testing the server
The go test command should test all of the API routes of the server and create/read/update/delete
users from the database.

    go test

#Frameworks and Tools
###Server
Martini is simple, uses dependency injection and enables quick prototyping.
I haven't tried other libraries, but martini is very similar to Express which I like and I was
somewhat familiar with it.
https://github.com/go-martini/martini


###Database
Sqlite3 wrapped by gorm
I wanted to try out an ORM in a statically typed language so I went with gorm. Sure, there are a lot
of interface{} casts and a few nil dereferences but overall I think it's nice for a simple CRUD app.
I didn't want a heavyweight database so I went with sqlite for it's single file storage and ability
to use in memory tables for testing.
https://github.com/jinzhu/gorm

###Testing
net/http/httptest - I used this to setup a server with an in memory database and test it. Not a lot
of magic and very simple to understand.

#API

#Models

#Authentication

#Tests

