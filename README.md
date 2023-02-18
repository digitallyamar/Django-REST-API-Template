# Django-REST-API-Template
A template repo to get a quick start with using Django REST API


# How To Run?
This Django REST API template server is written using Python3. So make sure you have Python3 installed in your system.

Here are the steps to follow to get your Django REST API server up and running:

    Step 1: Clone the repo
            git clone https://github.com/digitallyamar/Django-REST-API-Template.git
            cd Django-REST-API-Template

    Step 2: Create Python virtual environment
            python3 -m venv venv
            source venv/bin/activate
    
    Step 3: Install required Django packages
            pip install django djangorestframework
    
    Step 4: We have created a new Django project called django_rest_api using the django-admin command startproject. Hence you see the directory called django_rest_api. But if you would like to create a new project with a different name, use the command:
            django-admin startproject <YOUR PROJECT NAME> .

    Step 5: We have created a sample Todo Django App using the django-admin command startapp. Hence you see the directory called todo.  But if you would like to create a new project with a different name, use the command:
            django-admin startapp <YOUR DJANGO APP NAME>
        
        ### Note: 
            1. When you create a new app, add an entry for it's config info in the INSTALLED_APPS array of the settings.py file.
            2. You will also need to define your own app model (Database model) in the app's models.py file.
            3. You will then need to create a migration file for your new app model using the command:
                python3 manage.py makemigrations <YOUR DJANGO APP NAME>
            4. Finally, apply the migrations using the command:
                python3 manage.py migrate
    
    Step 6: Create a serializer file to convert your database's model data to a readable serialized data that can be displayed to the end user. Refer to todo/serializers.py file for an example implementation.
    
    Step 7: Next, we decide what data to show to the users using the app's views.py file. So create and update <YOUR DJANGO APP NAME>/views.py file. Refer to our todo/views.py file for an example implementation.

    Step 8: Next, we will create an urls.py file to map a view to it's respective URL. You can refer to our todo/urls.py file for an example implementation. This file needs to be called from the project level urls.py file using the 'include' attribute. Refer to django_rest_api/urls.py file to find an example of how it is including our todo/urls.py file.

    Step 9: Finally add Django's rest framework app module to our project by including them in our INSTALLED_APPS array of the settings.py file.

    Step 10: All the required configurations should now be done. So all you need to do now is to run our Django REST API server using the command:
            python3 manage.py runserver

        You should now have your server up and running. You can visit the following url to access serialized Model data of your Todo app at the url:
            http://127.0.0.1:8000/api/todo/
