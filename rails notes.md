```
require "awesome_print”
ActiveRecord::Base.logger.level = :debug
ap User.find(1)
```
find user with specific email domain
```
u = User.where("email LIKE ?", "%@gmail.com").pluck(:email)
```

find local gem list
```
gem list
bundle show devise
```
