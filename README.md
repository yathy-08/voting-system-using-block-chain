# 🗳️ Voting System using Blockchain

A secure web platform where users can cast votes digitally. Built with **Python Django**, this project integrates **blockchain technology** to ensure vote integrity, transparency, and reliability.

---

## 🚀 Features

- ✅ Secure voting via blockchain
- ✅ OTP-based voter authentication
- ✅ Real-time vote count and result display
- ✅ Automatic winner email notification
- ✅ Dummy data generation for testing
- ✅ Professional and responsive UI

---

## 📸 Screenshots

### Home Page / Login
![Home Page](images/home_page.png)

### Voting Page
![Voting Page](images/voting_page.png)

### Vote Confirmation
![Vote Confirmation](images/vote_confirmation.png)

### Show Results
![Show Results](images/show_results.png)

### Blockchain Verification (Optional)
![Blockchain Verification](images/blockchain_verification.png)

---

## 🛠️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/voting-system-using-block-chain.git
   cd voting-system-using-block-chain

2. Make sure you are connected to the internet.
3. Install all the (pip) dependency packages (main packages are listed in `requirements.txt`).
4. Locate `EMAIL_ADDRESS` and `EMAIL_PASSWORD` variable in `Election/settings.py` file and assign your valid credentials. (See [References](#EmailCredentials))
5. Make sure email sending is allowed (while development process sending email every time is not a good idea because API allows us to send email only for limited no. of times.).


​		For this make sure `send_otp()` method in `views.py` file looks like this:

```python
...
[success, result] = send_email_otp(email_input)
# [success, result] = [True, '0']
...
```

​		and `get_parties()` method in same file (`views.py`) looks like this:

```python
...
send_email_private_key(request.session['email-id'], private_key)
# print(private_key)
...
```

6. Locate `manage.py` file and run `python manage.py runserver` in the same directory.

7. Locate the URL provided in the terminal and access that. by default it is [http://127.0.0.1:8000](http://127.0.0.1:8000).