##Assessing your grasp of Rails fundamentals.

#In the command prompt:

##What command do you use to make ActiveRecord calls in the rails console? 
 **rails c**

##How do you exit the rails console?
**exit**

##What is the command used in the terminal to create a new rails app (ex. I want to create an app call my_app)?
**rails new my_app**

##How do you start the local rails server from the command prompt?
**rails s**

##How do you stop the rails server from running?
**ctrl-c**

##How do you generate:

###A model called Post with attributes username, email, and entry?

**rails g model Post username email entry:text**

###A controller Products with  index and about pages?

**rails g controller Product index about**

###A model, view, and controller called Vehicle with parameters name, price, and category ?
**rails g scaffold Vehicle name price:decimal category**

##How do you add fields (columns) to a table that already exists (i.e., I want to add the field year to my Vehicle table)?

**rails g migration AddYearToVehicles year:integer**

##What command must be ran after creating or modifying a table (i.e., after adding a new column)?
**rails db:migrate**

##How do you undo a generated resource?
**rails d scaffold RESOURCE_NAME**

##How do you undo a migration?
**rails db:rollback** - rolls back the latest migration

##How do you delete all the records in your databases from the command prompt?
**rails db:reset**

##In the rails app:

###What are the subdirectories contained in the ‘app’ directory?
**assets**
**channels**
**controllers**
**helpers**
**jobs**
**mailer**
**models**
**views**
###In what directory do we find our “routes.rb” file?
**config**

###What is the name of the controller that “controls” our entire application?
**application_controller.rb**

###What is the name of the view that allows us to show content on all the views of our application?
**application.html.erb**

###What is the purpose of the “<%= yield %> in the application.html.erb?
**It renders the content of our of individual html pages**

###What does the “.erb” extension mean?
**embedded ruby**

##How do we print content to the screen in rails?
**<%=  %>**

##How does data move from our database to the client area (screen)?
**Through the controller and the use of instance variables**

##What is a Ruby Gem?
**packaged code made to work with Rails and Ruby that extends the functionality of your Ruby program or Rails app.**

##What command must be ran in the terminal after modifying the Gemfile.rb?
**bundle install**

##Where are ActiveRecord statement usually found?
**in the controller**

##What does it mean to “render”?
**what we use to bring partial forms or code into other areas of our app. You can only render partials.**

##Associations

##How many database tables are needed for a many-to-many association?
**3**

##What is that additional table called?
**Join Table**

##What files state our association declarations?
**model file**

##Gems

##What are the steps for adding Bootstrap to a rails app (include file names and commands in terminal)?

**Gemfile.rb => gem 'bootstrap-sass', gem 'jquery-rails'**
**terminal => bundle install**
**app/stylesheets/application.css => @import 'bootstrap-sprockets', @import 'bootstrap'**
**change application.css to application.scss**
**app/stylesheets/application.js => //= require jquery, //= require jquery_ujs, //= require bootstrap-sprockets.  Remove //= rails-ujs**
**app/views/layouts/application.html.erb => add a <div class='container'> around the <%= yield %>**


##What are the steps for adding Devise to a rails app?
**Gemfile.rb => gem 'devise'**
**Terminal => bundle install**
**Terminal => rails g devise:install**
**Termianl => rails g devise User**
**rails db:migrate**


##What is the command need to gain access to the views used by Devise?
**rails g devise:views**

##What is the model used by Devise to store user information?
**user.rb**

##What controller is used to interact with the Devise model?
**application_controller.rb**