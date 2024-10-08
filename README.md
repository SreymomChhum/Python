### Supported Python Versions

This library supports the following Python implementations:

- Python 3.11


## Installation

Install from PyPi using [pip](https:n//pip.pypa.io/en/latest/), a
package manager for Python.

```shell
pip3 install plasgate
```

### Test your installation

Try sending yourself an SMS message. Save the following code sample to your computer with a text editor. Be sure to update the `account_sid`, and `auth_token` from your [Plasgate account](https://cloud.plasgate.com/).

```python
from twilio.rest import Client

# Your Account private_key and x-secret_key from plasgate
account_sid = "your_private_key"
auth_token  = "your_X_secret_key"

client = Client(account_sid, auth_token)

message = client.messages.create(
    to="+85558675309",
    sender="text_your_sender_name",
    content="text_your_message")

print(message.sid)
```

After a brief delay, you will receive the text message on your phone.

> **Warning**
> It's okay to hardcode your credentials when testing locally, but you should use environment variables to keep them secret before committing any code or deploying to production. Check out [How to Set Environment Variables](https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html) for more information.
