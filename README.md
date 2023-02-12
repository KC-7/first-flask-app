# KC-7 First Flask Project

[Click here to view the live site!](https://kc-flask-app.herokuapp.com/)

## Scotland Auto Spa Web Application

A website for a fictional car detailing company. This web application was created using Flask, a Python web framework. The following sections will explain the various techniques and languages used in the project.

------

## Table of Contents
- [Scotland Auto Spa Web Application](#scotland-auto-spa-web-application)
- [Flask Framework](#flask-framework)
- [Structure](#structure)
- [Route Decorators](#route-decorators)
- [JSON Data](#json-data)
- [Jinja2 Templates](#jinja2-templates)
- [Flash Messages](#flash-messages)
- [Libraries](#libraries)
- [Future Improvements](#future-improvements)
- [How to Run](#how-to-run)
- [Deployment](#deployment)
- [Conclusion](#conclusion)
- [Credits](#credits)


------

## Flask Framework
The Flask framework was used to build the entire web application. Flask allows developers to easily create web applications with Python, providing a simple structure and a variety of built-in tools and functionalities.

------

## Structure
- `run.py` contains the logic for the Flask app
- `base.html` serves as a base template for other templates to extend
- `index.html`, `about.html`, `contact.html`, `careers.html` are the templates for the respective pages
- `data/company.json` contains the data for the About Us page
- `static/` folder contains static files such as stylesheets and images
- `templates/` folder contains the HTML templates

------

## Route Decorators
Flask uses route decorators to specify the URL and corresponding function that should be triggered when the URL is requested. In this project, the following route decorators were used:

```
  @app.route("/")
  def index():
  ...

  @app.route("/about")
  def about():
  ...

  @app.route("/about/<member_name>")
  def about_member(member_name):
  ...

  @app.route("/contact", methods=["GET", "POST"])
  def contact():
  ...

  @app.route("/careers")
  def careers():
  ...
 ```

------

## JSON Data
JSON (JavaScript Object Notation) data was used to store information about the company and its members. This information is then retrieved and passed to the templates to be displayed on the about and member pages. The following code retrieves and loads the JSON data from the company.json file:

  `with open("data/company.json", "r") as json_data:
      data = json.load(json_data)`

------

## Jinja2 Templates
Jinja2 is a template engine for Python that was used in this project to create the HTML templates. Jinja2 templates allow dynamic content to be rendered and displayed in a web page

------

## Flash Messages
The flash function in Flask was used to display success messages on the contact page after a form has been submitted. The following code shows the implementation of the flash message in the contact function:

  `if request.method == "POST":
      flash("Thanks {}, we have received your message!".format(
          request.form.get("name")))`

------

## Libraries
The following CSS and JavaScript libraries were used to enhance the look and functionality of the web pages:

- Bootstrap (framework)
- Clean Blog (template)

------

## Future Improvements

- Update and tailor the site content to reflect a faux car cleaning company. 

- Set up emails to send to a specific company address. 

- Replace careers with services information, utilising same methods used for employee info. 

------

## How to Run

To run this project locally, you need to have Python installed. 
Once you have cloned this repository, run the following command in the terminal/command prompt:

  `pip install -r requirements.txt`

This will install the required packages. After that, you can:

Type `python3 run.py`,

A blue button should appear, click: _Make Public_,

Another blue button should appear, click: _Open Browser_.

------

## Deployment

The  site was deployed using Heroku. 

------

## Conclusion

This website was built using Flask, a Python web framework. It utilized HTML, CSS, and JavaScript to enhance the user experience and add styling to the pages. The site also used JSON data and Jinja templates to dynamically display information about the company. 

By utilizing these technologies, the site was able to provide a comprehensive and engaging experience for the users. This project showcased the power of Flask and its ability to create a full-featured website, complete with dynamic content, contact forms, and easy navigation.

-------

## Credits

- I created the website by using information learned from the Code Institute, this website is based off their Thorin and Co example project. 

- The [Clean Blog Template from StartBootstrap.com](https://startbootstrap.com/previews/clean-blog) was used for this project as a template. 

- This readme was partially created by passing snips of code from the project into [ChatGPT](https://chat.openai.com/chat), this was useful to create and document this project for future reference.

