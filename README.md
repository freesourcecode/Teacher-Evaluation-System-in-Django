# Teacher Evaluation System Project in Django with Source Code

The **Teacher Evaluation System in Django created based on Python, Django, and SQLITE3 Database**.

The **Teacher Evaluation System** is a simple project for the Students will only rate the faculty members who are assigned to their class per subject, which means that if a faculty member teaches the class two subjects, the class can rate the instructor twice.

A **Teacher Evaluation System** is even if the assessment is still in progress, faculty users are only able to display their evaluation results.

The system’s assessment will be based on the system’s default academic year, which can be changed on the academic page by the administrator.

In this method, the assessment questionnaire is interactive, which means that the administrator will generate the questions and order them according to the evaluation criteria.

_This **Teacher Evaluation System in Django** is an easy project for beginners to learn how to build a web-based python Django project_.

We will provide you with the complete source code and database for the python project so that you can easily install it on your machine and learn how to program in Python Django.

>[!NOTE]
> To start creating a **Teacher Evaluation System in Python Django**, makes sure that you have PyCharm Professional IDE Installed in your computer.

## Faculty Features

*  **Dashboard**

For the faculty dashboard, you will be able to all the basic access in the whole system.

Such as view all evaluation and delete evaluation.

* **View Evaluation Result**

The faculty can view all evaluation result

*  **Login and Logout**

By default one of the security features of this system is the secure login and logout system.

## Student Features

*  **Login Page**

Student enter their website credentials on this page to gain access in order to log in.

* **Register Page**

The page where new customer created their login credentials for the website.

*  **Home Page**

When student visit the website, this is the system’s default page.

* **Evaluate Faculty**

The student users are is permitted only to evaluate the faculties that are assigned to their class per subject.

## How to Create a Teacher Evaluation System in Django?

Here are the steps on **how to create a Teacher Evaluation System Project in Django**.

1. **Open file**.

First, open “pycharm professional” after that click “file” and click “new project”.

![image](https://github.com/user-attachments/assets/f5d91102-f4bb-414f-8edc-07ce035083bf)


2. **Choose Django**.

Next, after click “new project”, choose “Django” and click.

![image](https://github.com/user-attachments/assets/ae38f7e1-72c2-4292-b9f2-463e8d8bf759)


3. **Select file location**.

Then, select a file location wherever you want.

4. **Create application name**.

After that, name your application.

5. **Click create**.

Finish creating project by clicking “create” button.

![image](https://github.com/user-attachments/assets/ddec6d28-0db7-47ec-b076-06e4986c15e8)

6. **Start Coding**.

Finally, we will now start adding functionality to our Django Framework by adding some functional codes.

## Functionality and Codes

* **Create template for the login page**

In this section, we will learn on how create a templates for the login page. 

To start with, add the following code in your login.html under the folder of review/templates/review.


``` 
{% extends 'Home/index.html' %}
{% load crispy_forms_tags %}
{% block content %}
    <div style="margin-top: 2cm; margin-left: 10cm; margin-right: 10cm;">
        <form method="POST">
            {% csrf_token %}
            <legend class="text-center mt-4">Login as admin</legend>
            {{ form|crispy }}
            <div class="form-group">
                <button class="btn btn-success" type="submit">Login</button>
            </div>
        </form>
        <a href="{% url 'HomeView' %}">Home</a>
    </div>
{% endblock content %}
```

* **Create template for the details evaluation form**

In this section, we will learn on how create a templates for the details evaluation form. 

To start with, add the following code in your detail_feedback.html under the folder of review/templates/review.

```
{% extends 'Home/index.html' %}
{% block content %}
    <div class="container">
        <h1 class="text-center py-3">Details of Evaluation</h1>
        <div class="card p-4 m-4">

            <p style="font-size: 23px;"><strong>Teacher Name:</strong><br>{{ feedback.teacher_name }}</p>
            <p style="font-size: 23px;"><strong>Dated on:</strong><br>{{ feedback.date_submitted|date:'d F, Y H:i e' }}</p>
            <hr class="p-0 m-0 mb-3">
            <p style="font-size: 23px;"><strong>The teacher is punctual in coming to class:</strong><br>{{ feedback.punctuality }}</p>
            <p style="font-size: 23px;"><strong>The teacher completes portions at the appropriate time:</strong><br>{{ feedback.portion }}</p>
            <p style="font-size: 23px;"><strong>The teacher takes in effort to clear your doubts:</strong><br>{{ feedback.doubt }}</p>
            <p style="font-size: 23px;"><strong>The teacher makes the class interactive:</strong><br>{{ feedback.interactive }}</p>
            <p style="font-size: 23px;"><strong>Other Comments:</strong><br>{{ feedback.comments }}</p>

            <div class="row pt-3">
                <a class="btn btn-outline-primary ml-4 mr-4 col" role="button" href="{% url 'ListFeedbackView' %}">Back to all Evaluation</a>
                <!-- TODO: Add a confirmation modal -->
                <!-- TODO: Add link to delete feedback and go to all feedbacks -->
                <a class="btn btn-outline-danger mr-4 col" role="button" href="{% url 'DeleteFeedbackView' feedback.id %}">Delete this Evaluation</a>
                <a class="btn btn-outline-secondary mr-4 col" role="button" href="{% url 'LogoutView' %}">Logout</a>
            </div>
        </div>
    </div>
{% endblock content %}
```


* **Create template for the delete confirmation**

In this section, we will learn on how create a templates for the delete confirmation. 

To start with, add the following code in your confirm_delete.html under the folder of review/templates/review.

```
{% extends 'Home/index.html' %}
{% block content %}
    <!-- TODO: Switch this to a modal -->
    <div class="container">
        <div class="row py-3 text-center">
            <p class="lead">Are you sure you want to delete this feedback?</p>
        </div>
        <form method="POST">
            {% csrf_token %}
            <button class="btn btn-danger mr-3" type="submit">Yes, delete</button>
            <a class="btn btn-secondary" role="button" href="{% url 'FeedbackDetailView' feedback.id %}">cancel</a>
        </form>
    </div>
{% endblock content %}
```
### 📌Here's the full documentation for the [Teacher Evaluation System Project in Django](https://itsourcecode.com/free-projects/python-projects/teacher-evaluation-system-project-in-django-with-source-code/)



