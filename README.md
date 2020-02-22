# AntiCoding
The app for the AntiCoding Event organised anually by CSA during APOGEE.

# Installing and running the application (For ubuntu and windows)
Guaranteed to work with python 3.5 but not above.

It is advisable to use Anaconda. Follow these instructions to install Anaconda and python 3.5 in the environment:
1. Install Anaconda(https://www.anaconda.com/distribution/).
2. Create a new conda environment and install python 3.5: `$conda create -n NAME_OF_ENV python=3.5`, where `NAME_OF_ENV` is to be replaced by your preferred name.
3. The environment can be activated by: `$conda activate NAME_OF_ENV` and deactivated by `NAME_OF_ENV`.

Change the directory to the anticoding folder and enable the environment, then follow these instructions:
1. `$pip install -r requirements.txt`	
2. `$python manage.py migrate`
3. `$python manage.py createsuperuser` and enter details of the administrator. Using the credentials you can login as admin ('/admin'/).
4. `$python manage.py runserver` , this will start the application on 127.0.0.1:8000/app/ or localhost:8000/app/. This won't allow other computers to connect to the server.
5. Or you can also `$python manage.py runserver <IP address>:<port>` . You can find the IP address using ipconfig(Windows)/ifconfig(Ubuntu). Port can be anything.
	Eg: `$python manage.py runserver 192.168.0.1:8900`. This will allow other computers to connect to the server using the same ip address and port(192.168.0.1:8900).
6. Or you can simply run `$python manage.py runserver 0.0.0.0:8000`. And other computers to connect to the server using the server ip address and port as 8000.(You can find the IP address using ipconfig(Windows)/ifconfig(Ubuntu))
