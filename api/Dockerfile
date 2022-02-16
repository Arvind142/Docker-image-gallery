#base image 
FROM python:3.9

#working directory
WORKDIR /app 

#expose PORT for connectivity
EXPOSE 5050

#copyign requirements
COPY Pipfile Pipfile.lock ./

#installing pipenv
RUN pip install pipenv

#copying requiements to file
RUN pipenv lock --requirements > requirements.txt

#installing dependencies
RUN pip install -r requirements.txt

#copying all files
COPY . ./

#running app
CMD ["python", "main.py"]