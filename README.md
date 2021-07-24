# SCA-Cloud-School-Application
## Built With

- Docker
- Nginx
- HTML
- VS Code

## Docker Repository Link

[sca_app](https://hub.docker.com/repository/docker/enkodes/sca_app)

## Getting Started

To get a local copy up and running follow these simple example steps.

**Setup**

- Run the command `git clone https://github.com/enkog/SCA-Cloud-School-Application.git` on your terminal to clone this      repository.<br>
- Change to the project directory by entering `cd SCA-Cloud-School-Application` in the terminal<br>

## Steps for Deploying Webpage with Docker and Nginx
 - Create a directory<br>
 - In your directory, create an `index.html` and a `Dockerfile` file.<br>
 - Place the contents below into the Dockerfile<br>

    `FROM nginx:alpine
    COPY . /usr/share/nginx/html`

- Run the command `docker build -t html-server-image:v2 .` to build the docker image for the HTML server.<br>
- Confirm that this has worked by running the command:  <br>
    
    `docker images` <br>

- Run the command `docker run -d -p 80:80 html-server-image:v2` to run the HTML container server.<br>
- Run the command `curl localhost:80` to ensure the server is running.<br>

## Pushing the image to docker hub
- Create a public repository on `https://hub.docker.com/` called `sca_app`<br>
- Retag the docker image using the command `docker tag html-server-image:v2 enkodes/sca_app:latest`<br>
- Login to docker hub by running the command `docker login`<br>
- Run the command `docker push enkodes/sca_app:latest` to push the image to docker hub.

### Usage

Open `http://localhost` in your browser.

## Author

👤 **Oguadinma Nkiruka Ngozika**

-   Github: [@enkog](https://github.com/enkog)
-   Linkedin: [@enkog](https://www.linkedin.com/in/enkog/)
-   Twitter: [@enkodes](https://twitter.com/enkodes)
