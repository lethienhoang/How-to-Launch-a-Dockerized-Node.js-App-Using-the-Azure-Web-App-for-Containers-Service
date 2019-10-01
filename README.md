# How to Launch a Dockerized Node.js App Using the Azure Web App for Containers Service
1. Go to portal of Azure
2. Search "Container Registry"
3. Create "Container Registry" with some fields (registry name, subscription,...)
4. Open powershell 
5. Login to "Container Registry" just created. command line here

docker login yourregistryname.azurecr.io --username yourusername
Password:
Login Succeeded

6. We're logged in and navigate to the firectory of nodejs sources
7. Create a docker image. command line here

docker build -t yourregistryname.azurecr.io/demo-app:latest .

this is will build the contents of the local and it'll be storing to yourregistryname.azurecr.io/

8. We can push this image to the "Container Registry"

docker push yourregistryname.azurecr.io/demo-app:latest

9. Check your images is showed up on yourregistryname.azurecr.io/

docker images

10. Create Web App for Container Service

11. After enter some information then go to Azure Container Registry tab
12. Select Registry dropdown => pick your registry
13. Create
14. Waiting and see your results

