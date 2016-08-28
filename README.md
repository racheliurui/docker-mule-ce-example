# Example of Mule app running on Dockerised Mule CE server

This is the companion project for [Dock Tales: Mule-In-A-Container
](http://www.sixtree.com.au/articles/2015/dock-tales-mule/) blog post.

# Updated 
by Rachel with
1) changing the version to Mule CE 3.8 (jdk 1.8)
2) docker image name updated to mule-ce-3.8

Build the image

	# docker build --tag mule-ce-3.8 .

Run the container

	# docker run -it -p 8080:9000 -v /data/mule-app:/opt/mule/logs -e "SAMPLE_USER_NAME=rachel" mule-ce-3.8

Verify the app

	curl localhost:8080/test

Should return

	{ "message": "Hello, rachel" }	
