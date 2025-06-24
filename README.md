# # prompt: seanybaby1122.github.io

# There is no direct way to "open" a website within a Colab notebook's runtime.
# However, you can use Python to make a request to the website or display it using an iframe.

# Method 1: Make a request to the website (to check if it's accessible or get content)
import requests

try:
    response = requests.get("https://seanybaby1122.github.io")
    if response.status_code == 200:
        print("Website is accessible. Status code:", response.status_code)
        # You can optionally print the content
        # print(response.text)
    else:
        print(f"Failed to access website. Status code: {response.status_code}")
except requests.exceptions.RequestException as e:
    print(f"An error occurred while accessing the website: {e}")

# Method 2: Display the website in an iframe (might not work reliably due to security restrictions)
# from IPython.display import IFrame
# IFrame("https://seanybaby1122.github.io", width=800, height=600)

# Method 3: Open the link in a new browser tab (user action required)
# from IPython.display import display, HTML
# display(HTML('<a href="https://seanybaby1122.github.io" target="_blank">Open seanybaby1122.github.io</a>'))