## Create your first Rails app
Install Rails using this guide found at
www.installrails.com

Check your Rails version
```
$ rails -v
```
Create a new Rails app
```
$ rails new pinteresting
$ cd pinteresting
```
## Git
#### Setup Git on a new computer
```
$ git config --global user.name “Michael Scott”
$ git config --global user.name
$ git config --global user.email “mscott@dundermifflin.com"
$ git config --global user.email
```
#### Setup Git for a specific app
```
$ git init
$ git status
$ git add .
$ git commit -am “first commit"
```
## GitHub
#### Generate SSH keys

The SSH key verifies your identity on your computer (that you are who you say who you are) when you upload. Follow the instructions on GitHub: https://help.github.com/articles/generating-ssh-keys

Install SSH key using command line:

```
$ ssh-keygen -t rsa -C "your\_email@example.com"
$ ssh-add id\_rsa
```

You will then be asked to create a password for this key

#### Follow instructions on GitHub website

- create a free account
- create repo on GitHub website
- link repo using command line

## Create your homepage

Run the Rails server

```
$ rails server
```

- go to localhost:3000 in a web browser
- open up a new terminal tab (cmd+t on Mac)

#### Create a new page

```
$ rails generate controller pages home
```

#### Add some text to this new page

app/views/pages/home.html.erb

```html
<h1>Welcome to my app!<h1> <p>Sign up here<p>
```

$ git status $ git add . $ git commit -am “create home page”

#### Setup the root path using Routes

config/routes.rb

replace:
```ruby
get "pages/home"
```
with:
```ruby
root "pages#home"
```
