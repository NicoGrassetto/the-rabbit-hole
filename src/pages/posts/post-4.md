---
layout: ../../layouts/MarkdownPostLayout.astro
title: Building an API with Python and Flask
author: Nico Grassetto
description: "Learn how to create a simple API using Python and Flask."
image:
    url: "https://flask.palletsprojects.com/en/2.3.x/_images/flask-logo.png"
    alt: "Flask logo"
pubDate: 2023-10-01
tags: ["python", "flask", "api", "tutorial"]
---
Flask is a lightweight and powerful web framework for Python. In this tutorial, we will walk through the steps to create a simple API.

## Setting Up Flask

First, install Flask using pip:

```bash
pip install flask
```

## Creating a Basic API

Create a file named `app.py` and add the following code:

```python
from flask import Flask, jsonify

app = Flask(__name__)

@app.route('/api', methods=['GET'])
def get_data():
    return jsonify({"message": "Hello, World!"})

if __name__ == '__main__':
    app.run(debug=True)
```

## Running the API

Run the API with:

```bash
python app.py
```

Visit `http://127.0.0.1:5000/api` in your browser, and you should see:

```json
{"message": "Hello, World!"}
```

## Conclusion

Flask makes it easy to build APIs quickly. You can extend this example by adding more routes, handling different HTTP methods, and integrating with a database.