## Django Dynamic Url Creation and  Messages generation
> ### Dynamic Url Creation:
  - #### What is a URL?
    <p>A URL is a web address. You can see a URL every time you visit a website – it is visible in your browser's address bar.(Yes!     127.0.0.1:8000 is a URL! And localhost:8000 is also a URL! And https://github.com/ is also a URL! )</p>
    
<img src="url.png" alt="url image"/>
 <p>Every page on the Internet needs its own URL. This way your application knows what it should show to a user.In Django, we use something called URL configuration.URL configuration is a set of patterns that Django will try to match the requested URL to find the correct view.</p>
  
  - #### How do URLs work in Django?
  <p>Let's open up the yourproject/urls.py file in your code editor like SublimeTool and see what it looks like:</p>
  
  <img src="urlsconf.png" alt="urlconf image"/>
  
  <p>As you can see, Django has already put something here for us.</p>
  <p>The admin URL, is already here:</p>
  <img src="urladmin.png" alt="urladmin image"/>
  
  <p>This line means that URL that starts with admin/, Django will find a corresponding view.</p>
   
  <img src="urladminlogin.png" alt="urladminlogin image"/>
  
  - #### Your first Django URL!
  <p>we can add our first URL pattern:</p>
  -<p> in urls.py for creating url we will use path function</p>
  -<p> in urls.py ,we have to import views from yourapp for that add this line in urls.py</p>
          - **'from appaname import views'**
          - example: 
                 > <p>for example my appname is **myapp** then</p>
                    - **'from myapp import views'** 
  - <p> for that path we will give different values like</p>
          - **path('urlname/',views.funtionname,name='nameoftheurl'),**
          - example: 
                  - **path('msg/',views.msg,name='msg'),**
   -it looks like(urls.py):
   <img src="msg.png" alt="msg image"/>
   - in views.py, we have to import HttpResponse for that add this line in views.py
            **from django.http import HttpResponse**
   -<p> in views.py we have add a function with name msg</p>
   def msg(request):
    return HttpResponse('welcome to all')
    
   > in this function, request is a default parameter,we can't change that.
   - it looks like:
   <img src="defmsg.png" alt="defmsg image"/>
   
   - save the changes  and start server using **python manage.py runserver**
   - then open chrome **localhost:8000/url**
   - example:
            - **localhost:8000/msg**
   - then we get OUTPUT it looks like:
   <img src="msgop.png" alt="msgop image"/>
  
       
    
 
