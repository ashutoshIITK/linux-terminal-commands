# Using cURL command

	curl http://www.google.com

It returns HTML code.

### Getting some response e.g. JSON

	curl http://wesite.address

### Ger header of reponse with JSON

	curl -i http://website.address

### Post to a URL or HTTP request

	curl -d "first=Ash&last=Ku" http://website.address

### Updating using PUT
	curl -X PUT -d "first=Ash&last=Ku" http://website.address

### Delete using DELETE
	curl -X DELETE -d "first=Ash&last=Ku" http://website.address

### Provide Username and Password
	curl -u user:pass http://website.address

### Dowload response from a route
	curl -o test.jpg http://website.download

### Download to a JSON
	curl -o json_file.json http://website.address