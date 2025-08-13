<b>Portfolio Website with Flask</b></br>

Overview:</br>
This code creates a simple web application using the Flask framework. It includes a form on the main page where users can submit their name, email, and message. When the form is submitted, it shows a thank-you message with the user's name.</br>

Imports:</br>
<b>Flask</b>: The main framework for creating the web app.</br>
<b>render_template</b>: Renders HTML templates.</br>
<b>request</b>: Handles incoming request data (like form submissions).</br>
<b>redirect</b>: Redirects the user to a different URL.</br>
<b>url_for</b>: Generates URLs for routes.</br>
<b>flash</b>: Displays one-time messages to the user.</br>
<b>os</b>: Used to generate a random secret key.</br>

App Initialization:</br>
app = Flask(__name__)</br>
app.secret_key = os.urandom(24)</br>
- Creates a Flask application instance named `app`.</br>
- Sets a secret key used for session management and flashing messages, generated randomly for security.</br>

Route Definition:</br>
@app.route('/', methods=['GET', 'POST'])</br>
- Sets up the route `'/'` (the homepage).</br>
- Accepts both `GET` (to display the page) and `POST` (to handle form submission) requests.</br>

Function body:</br>
- Checks if the form was submitted via POST.</br>
- Retrieves form data: `name`, `email`, and `message`.</br>
- Uses `flash()` to display a personalized thank-you message.</br>
- Redirects the user back to the homepage to avoid form resubmission issues.</br>

Handling GET Request:</br>
return render_template('index.html')</br>
Renders the `index.html` template when the page is loaded via GET or after handling POST.</br>

Running the App:</br>
Runs the Flask app with debugging enabled, so errors will be shown in the browser.</br>

Summary:</br>
- The app serves a webpage (with a form in `index.html`).</br>
- When a user submits the form, it captures their info, flashes a thank-you message, and redirects back to the homepage.</br>
- The `flash()` message can be displayed in HTML template using Flask's flashing system.</br>

