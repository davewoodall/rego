NAME
---------------
  
rego

SYNOPSIS
---------------
  
rego ./files ./to ./watch -- command-to-run

INSTALL
---------------

gem install rego

DESCRIPTION
---------------
  
run arbitrary commands easily when files change

PARAMETERS
---------------

--help, -h 

EXAMPLES
---------------
  
```bash

  # say hai whenever the file foo.txt changes
  #
    ~> rego foo.txt -- echo hai

  # say hai whenever any file (recursively) in bar changes 
  #
    ~> rego ./bar/ -- echo hai

  # echo *the file that changed* when any file (recursively) in bar changes 
  #
    ~> rego ./bar/ -- echo "@ was changed"

  # run a specific test whenever anything in lib, test, app, or config changes
  # 
    ~> rego {lib,test,app,config} -- ruby -Itest ./test/units/foo_test.rb --name teh_test
  _Note there can be no spaces between files. {lib, test} won't work_
  # run a specific test whenever it, or your app, has changed
  #
    ~> rego ./test -- ruby -Itest @

```
