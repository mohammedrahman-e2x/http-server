# How to run

## Set up
1. Create an SSL directory in the root. `mkdir ssl`
2. `cd ssl`
3. Generate a self signed ssl: `openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 3650 -nodes -subj "/C=XX/ST=StateName/L=CityName/O=CompanyName/OU=CompanySectionName/CN=CommonNameOrHostname"`
4. `cd ..`

## Update hosts file
1. `cursor /etc/hosts` 
2. Add the following line: `127.0.0.1     abc.xyz`
   1. (abc.xyz could be anything you want)
3. Save (may need to be sudo)

## Run the http
1. Run this from the site root directory: `npm run start-https-proxy`

Now any site you have on localhost or 127.0.0.1 will be accessible on `https://abc.xyz`