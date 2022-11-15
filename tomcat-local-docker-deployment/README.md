# Local Tomcat & Docker Deployment
### Pre-requisites
* [VS Code Java Coding Pack](https://code.visualstudio.com/docs/languages/java#_install-visual-studio-code-for-java)
### Testing the .war Locally
1. Install the [Remote Server Protocol UI](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-rsp-ui) VS Code Plugin.

2. A tab named **Servers** should now appear in VSCode (on the bottom left-hand side). Click the icon to **Create a new server**. 

![image](https://user-images.githubusercontent.com/31021304/202042084-b6ddbfed-b3af-46e2-910f-95c584bf415c.png)

3. Follow the prompts after clicking **Create new server**. 
- For "Download server?: Choose **Yes**.

    ![image](https://user-images.githubusercontent.com/31021304/202042258-11d862c7-6d9d-4cf2-a5b7-2a564cf842f0.png)

- For "Please choose a server to download": Choose the latest version of **Apache Tomcat 9**

    ![image](https://user-images.githubusercontent.com/31021304/202042312-d8cba0a6-23c1-491a-b3e0-2c91a2bddc67.png)

- For "License URL": Choose **Continue**
- For "Do you agree to the license?": Choose **Yes (True)**

3. Start the Tomcat Server - right click on the new Tomcat Server and choose **Start Server**:
![image](https://user-images.githubusercontent.com/31021304/202043089-1473512d-2286-4a10-8470-17b48d173a4d.png)


4. Right Click your `ROOT.war` and choose **Run on server** - select the new Tomcat Server. When prompted for "Do you want to edit deployment parameters?": Choose **No**.

5. This will now deploy the `ROOT.war` to this Tomcat instance. If successfully deployed you should see the following UI when browsing `localhost:8080:`

![image](https://user-images.githubusercontent.com/31021304/202043587-af3255e1-5531-45ad-97b7-039ce52f82ca.png)


> **NOTE**: Deploying the WAR file can take up to a minute to succeed. You may see a HTTP 404 in the mean time.

* [Docker CLI](https://docs.docker.com/install/)

### Building with Docker

1. Clone the repository and navigate into the root of the repository:

1. Build the docker image:

    ```bash
    docker build -t dockertomcat:01 .
    ```

1. Run the image:

    ```bash
    docker run -d -p 8080:8080 dockertomcat:01
    ```

1. Once the container is running, navigate to `http://localhost:8080`

