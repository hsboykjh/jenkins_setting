# jenkins_setting
jenkins_setting

##jenkins setting in order to access remote server on ssh protocol

##1.Jenkins Server
###user change to jenkins ( jenkins service is running jenkins account not user ) 
<code>sudo su -s /bin/bash jenkins</code>

###generate new rsa key
<code>ssh-keygen -t rsa</code>

###start the ssh-agent in the background
<code>eval "$(ssh-agent -s)"</code>

###add rsa key to ssh agent
<code>ssh-add ~/.ssh/id_rsa</code>


##2.remote server
add jenkins rsa to ~/.ssh/authorized_keys

##3.Jenkins server
<code>ssh remote_server_address</code>

