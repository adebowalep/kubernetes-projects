<h1>Project: Deploying MongoDB and Express</h1>

<h2>Project Description</h2>
<p>The objective of this project is to set up two applications, MongoDB and Express, and enable communication between them in a Kubernetes cluster. To achieve this, a MongoDB deployment and an internal service are created, and an Express deployment requires credentials and a database URL. These are passed through environmental variables in a configuration file that uses a config map and secret. An external service is also created to allow external requests to access Express through a browser. The request flow starts from the browser and goes to the external service of Express, which forwards it to the Express pod. The pod connects to the internal service of MongoDB using the database URL and credentials for authentication.</p>

<h2>Purpose</h2>
<p>The purpose of this project is to provide a sample for deploying MongoDB and Express in a Kubernetes cluster and demonstrate how to establish communication between them.</p>

<p>The project contains the following files:</p>
	<ul>
		<li>README.md</li>
		<li>K8s-commands.md</li>
		<li>mongo-express.yaml</li>
		<li>mongo.yaml</li>
		<li>mongo-configmap.yaml</li>
		<li>mongo-secret.yaml</li>
	</ul>
	
<p>These files contain YAML code to create the necessary Kubernetes resources to deploy MongoDB and Express.</p>
	
<p>For more details on the commands used and the YAML files, refer to the K8s-commands.md file. To view the running pods, services, and secrets, use the "kubectl get" command. To debug issues, use the "kubectl describe" command or view the logs with "kubectl logs". To access the external service in minikube, use the "minikube service" command.</p>
	
<h2>Installation</h2>
<p>To install this project, you need to have a Kubernetes cluster and kubectl CLI installed on your machine.</p>

<ol>
	<li>Clone the repository: <code>git clone https://github.com/&lt;username&gt;/kubernetes-projects.git</code></li>
	<li>Change to the project directory: <code>cd kubernetes-projects/deploy-mongodb-express</code></li>
	<li>Deploy the project: <code>kubectl apply -f .</code></li>
</ol>


<h2>Usage</h2>
<p>After the deployment, you can access the Express application by running:</p>
<code>kubectl port-forward svc/express-service 3000:3000</code>
<p>Then open your browser and go to <a href="http://localhost:3000">http://localhost:3000</a>.</p>
	
<h2>License</h2>
<p>This project is licensed under the MIT license.</p>
</body>
</html>




