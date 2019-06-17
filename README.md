# hello_crow
Project is incompletely uploaded (on purpose).  
c++ web api project

Requirements
Atom (used for IDE, but any IDE is sufficient)
Docker
Heroku Account
MongoDb (both locally installed and mLab). Upload provided contacts.json into MongoDB

# Execute in Terminal
cd bbox

docker build --rm --no-cache -t bbox:latest .

cd ../

docker build --rm --no-cache -t hello_crow:latest .

docker run -p 18080:18080 -e PORT=18080 -e MONGODB_URI="mongodb://db_connection_goes_here" hello_crow:latest

# Browser
http://localhost:18080/contacts 

http://localhost:18081/contact/bwellsman6@dailymail.co.uk
