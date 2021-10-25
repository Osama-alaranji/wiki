### project name is ** wikibilal **
### app name is homepage
### app name members
#### static files and base will be in homepage app












## ----------------- for our team
### first for register in main urls file type  path('register/', include('django.contrib.auth.urls')),
### then type path('register/' , include("register.urls")),
### in views 
```python
from django.views import generic
from django.contrib.auth.forms import UserCreationForm
from django.urls import reverse_lazy
class UserRegisterView(generic.CreateView):
		form_class = UserCreationForm
		template_name = 'registration/signup.html'
		success_url = reverse_lazy('login')
```
### in urls 
```python 
from .views import UserRegisterView or 
 path('signup/', UserRegisterView.as_view() , name="signup"),
