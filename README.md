# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* Rails 2.6.5

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

# rails_admin
 Uma aplicação rails usando o rails admin - Estudo Ruby

rails g model User name:string document:string kind:integer status:integer notes:text
rails g model Client name:string company_name:string document:string email:string phone:string user:references notes:text status:integer
rails g model Address country:string city:string state:string neighborhood:string street:string number:string client:references user_id:integer
rails g model Product name:string description:text status:integer
rails g model Discount name:string description:text value:integer kind:integer status:integer
rails g model ProductQuantity product:references quantity:integer user:references
rails g model Sale client:references sale_date:date user:references discount:references notes:text
rails g model Comission sale:references value:decimal user:references status:integer note:text

rails db:migrate

bundle

rake db:seed
