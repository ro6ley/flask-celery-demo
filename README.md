[![HitCount](http://hits.dwyl.io/ro6ley/flask-celery-demo.svg)](http://hits.dwyl.io/ro6ley/flask-celery-demo)

# Ping! 

This repository contains the code for this [blogpost](https://stackabuse.com/asynchronous-tasks-using-flask-redis-and-celery/) on [StackAbuse](https://stackabuse.com/).

## Getting Started

### Prerequisites

Kindly ensure you have the following installed on your machine:

- [ ] [Python 3](https://realpython.com/installing-python/)
- [ ] [Pipenv](https://pipenv.readthedocs.io/en/latest/#install-pipenv-today)
- [ ] [Redis](http://redis.io/)
- [ ] Git
- [ ] An IDE or Editor of your choice

### Running the Application

1. Clone the repository
```
$ git clone https://github.com/ro6ley/flask-celery-demo.git
```

2. Check into the cloned repository
```
$ cd flask-celery-demo
```

3. If you are using Pipenv, setup the virtual environment and start it as follows:
```
$ pipenv install && pipenv shell
```

4. Install the requirements
```
$ pip install -r requirements.txt
```

4. Start the Flask app
```
$ python app.py
```

5. Start the Celery Cluster in a separate terminal window
```
$ celery worker -A app.client --loglevel=info
```

6. Start Flower in another separate terminal window
```
$ flower -A app.client --port=5555
```

7. Navigate to http://localhost:5000 and schedule an email with a message

8. Navigate to http://localhost:5555 to view the workers and scheduled messages under `Tasks` section

9. Check the receipient email inbox for the scheduled message after the time has ellapsed


## Contribution

Please feel free to raise issues using this [template](./.github/ISSUE_TEMPLATE.md) and I'll get back to you.

You can also fork the repository, make changes and submit a Pull Request using this [template](./.github/PULL_REQUEST_TEMPLATE.md).
