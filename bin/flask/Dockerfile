FROM python:3.8.2
LABEL maintainer="Sashwat K <sashwat0001@gmail.com>"

# Update and upgrade linux container
RUN apt-get -y update
RUN apt-get upgrade -y

# Clone sample Python Flask program
RUN git clone https://github.com/sashuu6/sample-python-flask.git /usr/share/sampleFlask/

# Requirements.txt
RUN pip3 install -r /usr/share/sampleFlask/requirements.txt

# Autoremove unnecessary tools
RUN apt-get autoremove -y

# Runs app.py
ENV FLASK_APP /usr/share/sampleFlask/app.py
ENV FLASK_RUN_HOST 0.0.0.0
CMD ["flask", "run"]