# Mails
#### Video Demo:

[My Final Project presentation](https://youtu.be/t65Autz2bog)

#### Description:
## CS50
>This was my final projectfor conclude the CS50 Introduction to Computer Sciense course.

>CS, python, flask, flask web framework, web development, Html, Css, CS50

## Explaining the project and the database
My final project is a website that allow the user register sending and receiveing mails
which are more important in present days mainly youth  for profeessional purpose.
 The user can login and logout as there wish of time. But the mails doesnot change and will be
 escaped of users. Individual Users information data stored in table **users**.


 >Home page

In the home page project title name ,***Cs50 Mails Sending*** and register , login link at top of the website.
**Register** link consist of form to enter our details like our email, password and confirm password ,to confirm or to fix the password we use confirm password .The main aim to fix the register link is we need to register again and again all the time .
 After a long time also we can only just login to access our past account by filling the form.`we need to remember the password & mailid`.
**login** link Consist of form to enter our email/gmail and password which we have entered same details of register form.
Login access us to our own account to check our mails which we receive , what we sent , what we want send to respective mails or we can able to send any mail to anyone to their mail only.

>index page

In the index page also have project title name,along with it Inbox ,compose,sent link has separate html pages. At another end of page logout link for login users.
at top of the page. Body of the page consist of Inbox by default.
**logout** link is to close our account . If we want to open our old account again then login with details.

>inbox page

In the inbox page is same as index page at the top bar. **Inbox** body has title Inbox and here we display the mails which we get from others with details of sender mailid, subject , timestamp with date and time. Horizontal line by separating the mails with details.
**View Details** button is to open the complete mail **Reply** is to give response to the respective mail which we are recevieing from others text our response for mail and hit reply .
we enter to index page i.e Inbox page Bydefault but our response can check at sent page .

>compose page[^1]

In the compose page  is same as index page at the top bar. **Compose** body has title Compose and here there is a form to send the mail.
From our mail sending mail to other mail by entering our mail at first, next we to enter mail to who we are sending their mailid next subject , atlast body i.e purpose of mailing.
Finally hit the send button to send the mail.


>sent page

In the sent page is same as index page at the top bar.**Sent** body has title Compose and here we display the mails which we send to others through  details of our mailid, respective opponent mailid, subject , timestamp with date and time.
Horizontal line by separating the mails with details.
**View Details** button is to open the complete mail and atlast we can see the reply button .
**Reply** is to give response to the respective mail which we have sent if we need or else igore to reply .
If we want sent mail again just text there and hit reply button then we redirect to index page  and check mail which we send mail  at sent page.


### Sql and sqlite3:
I needed three tables for my database:

- First, table users. Where I put hash  id ,username (email) ,password, notice that id must be a primary key here.

- Second, table emails. Here information of mail sender (sender), to user(to), aim to send the mail(subject), timestamp ,description of mail(body)





>Home page

In the home page project title name ,***Cs50 Mails Sending*** and register , login link at top of the website.
**Register** link consist of form to enter our details like our email, password and confirm password ,to confirm or to fix the password we use confirm password .The main aim to fix the register link is we need to register again and again all the time .
 After a long time also we can only just login to access our past account by filling the form.`we need to remember the password & mailid`.
**login** link Consist of form to enter our email/gmail and password which we have entered same details of register form.
Login access us to our own account to check our mails which we receive , what we sent , what we want send to respective mails or we can able to send any mail to anyone to their mail only.

>index page

In the index page also have project title name,along with it Inbox ,compose,sent link has separate html pages. At another end of page logout link for login users.
at top of the page. Body of the page consist of Inbox by default.
**logout** link is to close our account . If we want to open our old account again then login with details.

>inbox page

In the inbox page is same as index page at the top bar. **Inbox** body has title Inbox and here we display the mails which we get from others with details of sender mailid, subject , timestamp with date and time. Horizontal line by separating the mails with details.
**View Details** button is to open the complete mail **Reply** is to give response to the respective mail which we are recevieing from others text our response for mail and hit reply .
we enter to index page i.e Inbox page Bydefault but our response can check at sent page .

>compose page[^1]

In the compose page  is same as index page at the top bar. **Compose** body has title Compose and here there is a form to send the mail.
From our mail sending mail to other mail by entering our mail at first, next we to enter mail to who we are sending their mailid next subject , atlast body i.e purpose of mailing.
Finally hit the send button to send the mail.


>sent page

In the sent page is same as index page at the top bar.**Sent** body has title Compose and here we display the mails which we send to others through  details of our mailid, respective opponent mailid, subject , timestamp with date and time.
Horizontal line by separating the mails with details.
**View Details** button is to open the complete mail and atlast we can see the reply button .
**Reply** is to give response to the respective mail which we have sent if we need or else igore to reply .
If we want sent mail again just text there and hit reply button then we redirect to index page  and check mail which we send mail  at sent page.


### Storing Data of users and validations.
The input fields of emails have a client side validate, my database have a recepient ,subject, body fields ,if we won't
fill any one field then it won't allow us to move forward.
```python
 if request.method == "POST":
        emailId = request.form.get("emailId")
        emailDetailDB =  db.execute("SELECT * FROM emails WHERE id = ?", emailId)
        emailDetail = emailDetailDB[0]
        return render_template("reply.html",  emailDetail=emailDetail)

```


Validations for mail, subject, etc:
## Pictures
- Login and compose page

| Login | compose |
| :---: | :---: |


- Homepage and Responsive show case

| Homepage | reply |
| :---: | :---: |







