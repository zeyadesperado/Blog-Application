# Project:
	* Blog Application
# Project Discription:
	* Website For Creating Our Blogs.
# What You Should Do:
	1. Registration Page:
		* This page for registering the user into the App
		* This Page URL is `http://127.0.0.1:8000/register`
	2. Login Page:
		* This page for logging the user into the App
		* This Page URL is `http://127.0.0.1:8000/login`
	3. logout Page:
		* This is the page for logging out the user
		* This Page URL is `http://127.0.0.1:8000/logout`
    4. Home Page:
        * This Page is Used To Show:
          * If The User Logged Then It Will Show His Blogs Only in my blogs
        * This Page URL is `http://127.0.0.1:8000/myblogs`
          * If The User Not Logged It Will Show All Blogs Of All Users
        * This Page URL is `http://127.0.0.1:8000`
    5. Create Blog Page:
        * This Page Is Used To Create New Blog
        * This Page Url `http://127.0.0.1:8000/create`
    6. Show Blog Page:
        * This Page Is Used To Show User's Blogs
        * This Page Url `http://127.0.0.1:8000/myblogs`
    7. Update Blog Page:
        * This Page Is Used To Update Specific Blog Info Using `POST` Request
        * This Page Url `http://127.0.0.1:8000/edit/<int:blog_id>/`
    8. Delete Blog Page:
        * This Page Is Used To Delete Specific Blog Info
        * This Page Url `http://127.0.0.1:8000/delete/<int:blog_id>/`
    9. User is Allowed To ( Edit, Update,Delete ) His Blog
   > After The Blog is Created You Should Redirect To This Blog Page
# What You Need To Search On:
	* How To Use Postgresql in Django
	* Search About User Model in Django
# Side Notes:
	* Please Use Django **User** Model
# This Is The Database Tables
```sql
class Blog(models.Model):
    blog_title = models.CharField(max_length=70,default="Untitled")
    blog_text = models.CharField(max_length=500)
    blog_image = models.ImageField(upload_to='',null=True)
    timestamp = models.DateTimeField(auto_now_add=True)  
    author = models.ForeignKey(User, on_delete=models.CASCADE)
```
