# Django Tailwind Blog - A Developer Portfolio & Blog

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)

## Introduction
Regression Function
The regression function for the log-transformed GDP per capita (log_gdp_per_capita) is:

log(GDP per capita) = 0.9644 + 0.0023 ⋅ inflation − 0.0039 ⋅ gfcf + 0.0036 ⋅ gov_exp + 0.1198 ⋅ life_expectancy
log(GDP per capita)=0.9644+0.0023⋅inflation−0.0039⋅gfcf+0.0036⋅gov_exp+0.1198⋅life_expectancy

Where:

* **inflation** is the rate of inflation.
* **gfcf** is the gross fixed capital formation as a percentage of GDP.
* **gov_exp** is the government expenditure as a percentage of government expenditure.
* **life_expectancy** is the average life expectancy at birth.
## Interpretation of Coefficients
* **Constant (0.9644)**: This is the baseline value of log(GDP per capita) when all regressors are zero.
* **Inflation (0.0023)**: A 1% increase in inflation is associated with a 0.23% increase in GDP per capita, holding other variables constant.
* **Gross Fixed Capital Formation (gfcf) (-0.0039)**: A 1% increase in gfcf is associated with a 0.39% decrease in GDP per capita, holding other variables constant.
* **Government Expenditure (gov_exp) (0.0036)**: A 1% increase in government expenditure is associated with a 0.36% increase in GDP per capita, holding other variables constant.
* **Life Expectancy (0.1198)**: A 1-year increase in life expectancy is associated with a 11.98% increase in GDP per capita, holding other variables constant.
## Overall Model Performance
* **R-squared (0.999)**: The model explains 99.9% of the variability in the log of GDP per capita, indicating an excellent fit.
* **Adjusted R-squared (0.999)**: The adjusted R-squared, which accounts for the number of predictors in the model, also indicates an excellent fit.
* **F-statistic (2.130e+05)**: The high F-statistic value and its associated p-value (0.00) suggest that the overall model is statistically significant.
* **Durbin-Watson Statistic (2.021)**: This value, close to 2, indicates no significant autocorrelation in the residuals.
* **Jarque-Bera Test**: The Jarque-Bera test statistic (88.132) and its p-value (7.284e-20) indicate that the residuals are not normally distributed, which is a violation of one of the CLRM assumptions.

## Assumptions Check and Final Remarks
Several assumptions were checked to ensure the OLS estimators' desirable properties:

1. Linearity: Only life expectancy shows a linear relationship with the dependent variable, while other variables may exhibit non-linear patterns. This suggests a potential area for model improvement by considering non-linear transformations or interactions for the other variables.
2. Independence: The Durbin-Watson statistic suggests that there is no significant autocorrelation in the residuals.
3. Homoscedasticity: The Breusch-Pagan test indicates heteroscedasticity in the residuals (LM Statistic: 23.764, p-value: 8.906e-05). The use of WLS partially addresses this issue by providing robust standard errors.

4. Normality: The Jarque-Bera test indicates a violation of the normality assumption. This can be addressed by further data transformation or by employing robust statistical techniques.

### In conclusion, the final WLS model provides a strong fit for predicting the log of GDP per capita using the given regressors. Despite some violations of the classical assumptions, particularly in linearity and normality of residuals, the model remains robust and statistically significant. Further steps could involve addressing these violations to improve the model's reliability and predictive power.

![django-tailwind-blog-for-developers](https://user-images.githubusercontent.com/106135144/227858936-d4cbcb44-9ff4-4729-b0f0-6ede931b99e0.png)

## Table of Content
  * [Introduction](#introduction)
  * [Installation](#installation)
  * [Technologies Used](#technologies-used)
  * [Features](#features)
  * [Pages](#pages)
  * [Website Screenshots](#website-screenshots)
  * [Admin Screenshots](#admin-screenshots)
  * [Deployment](#deployment)
  * [Conclusion](#conclusion)
  
## Installation
1. Clone the repository:
```
git clone https://github.com/ashish-makes/django-tailwind-blog.git
```
2. Navigate to the project directory:
```
cd `django-tailwind-blog`
```
3. Create and activate a new virtual environment:
```
python -m venv env
source env/bin/activate
```
4. Install the project dependencies:
```
pip install -r requirements.txt
```
5. Install the `django-tailwind` module:
```
pip install django-tailwind
```
6. Add `tailwind` to your `INSTALLED_APPS` list in `settings.py`:
```python
INSTALLED_APPS = [
    # ...
    'tailwind',
    # ...
]
```
7. Run the Tailwind CSS configuration command:
```python
python manage.py tailwind init
```
8. Create the database tables:
```python
python manage.py migrate
```
9. Run the development server:
```python
python manage.py runserver
```

## Technologies used
1. HTML
2. CSS
3. JavaScript
4. Python

### Primary Modules used
1. Django==4.1.4
2. django-tailwind==3.4.0
3. whitenoise==6.3.0
4. psycopg2==2.9.5
5. django-tinymce==3.5.0

## Features
1. Responsive design using Tailwind CSS
2. Admin dashboard for managing blog posts and portfolio items
3. Contact form for sending messages to the site owner

## Pages
- `Home`: The landing page of the website, which displays a brief introduction and links to other pages.
- `About`: A page that provides information about the site owner, their background, and skills.
- `Contact`: A page that contains a contact form for visitors to send messages to the site owner.
- `Blog`: A page that displays a list of blog posts in reverse chronological order, with links to individual post pages.
- `Blog Post`: A page that displays the content of a single blog post, including the title, author, date, and content.
- `Projects`: A page that displays a list of portfolio projects, with links to individual project pages.
- `Project`: A page that displays the details of a single portfolio project, including the title, description, date, and any relevant images or links.
- `Categories`: A page that displays a list of blog post categories, with links to filtered lists of posts for each category.
- `Custom 404 Pages`: Custom error pages that display when a user navigates to a non-existent page or encounters an error.

## Website Screenshots
![127 0 0 1_8000_about](https://user-images.githubusercontent.com/106135144/218676693-b433a723-0569-4a5a-91e2-d2330659233d.png)

![127 0 0 1_8000_contact](https://user-images.githubusercontent.com/106135144/218676709-3924f790-32db-46f3-a1b5-bf1907506751.png)

![127 0 0 1_8000_blog](https://user-images.githubusercontent.com/106135144/218676733-bc2313e9-9721-4f4b-9fd8-ab7cfa939221.png)

![127 0 0 1_8000_projects](https://user-images.githubusercontent.com/106135144/218676756-3770e70e-149b-48ae-af50-44d1ee43aed6.png)

![127 0 0 1_8000_projectsk](https://user-images.githubusercontent.com/106135144/218676780-62e72dd7-d2e4-4ef9-9b2b-aea25abf625d.png)

## Admin Screenshots
![127 0 0 1_8000_admin_](https://user-images.githubusercontent.com/106135144/218730427-1aad64b4-65ff-44e4-babf-840d200919fa.png)

![127 0 0 1_8000_admin_home_blog_](https://user-images.githubusercontent.com/106135144/218730473-d914186d-eabf-4ff9-bc45-dd98c024cfb5.png)

![127 0 0 1_8000_admin_home_blog_7_change_](https://user-images.githubusercontent.com/106135144/218730503-f4027aeb-7579-4fc6-8fa4-5331201931e8.png)

## Deployment
To deploy this project to a web server, you can follow these general steps:

1. Set up a web server that can run Python applications. This could be a VPS, a PaaS like Heroku, or a cloud-based server like AWS.
2. Clone the repository to your server:
```
git clone https://github.com/ashish-makes/django-tailwind-blog.git
```
3. Install the project dependencies on your server using `pip`:
```
pip install -r requirements.txt
```
4. Set up a database for the project, if necessary. You can use a database like PostgreSQL, MySQL, or SQLite, depending on your needs.
5. Configure the settings.py file with your server's settings:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'mydatabase',
        'USER': 'mydatabaseuser',
        'PASSWORD': 'mypassword',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}

STATIC_ROOT = '/var/www/static/'
MEDIA_ROOT = '/var/www/media/'

ALLOWED_HOSTS = ['example.com', 'www.example.com']
```
The DATABASES setting specifies the database connection details. In this example, we're using PostgreSQL with a database named `mydatabase`, a user named `mydatabaseuser`, and a password of `mypassword`. The `STATIC_ROOT` and `MEDIA_ROOT` settings specify the file paths where static files and media files will be stored. The `ALLOWED_HOSTS` setting is a list of domain names that the application is allowed to serve.
6. Run the python manage.py collectstatic command to collect all the static files into the STATIC_ROOT directory:
```python
python manage.py collectstatic
```
7. Start the Django development server, or set up a production server using a WSGI server like uWSGI or Gunicorn.
```python
python manage.py runserver
```
8. Access the website using your server's IP address or domain name, and the port number of the server if necessary. For example, if you're running the development server on port 8000, you can access the website at `http://your-server-ip:8000/`.
