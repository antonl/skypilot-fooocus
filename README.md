# Fooocus on AWS

Here's how you run Fooocus on AWS if you don't own a GPU.

1. Install skypilot somehow. I've provided an environment.yml for you
   to install it using conda.
2. Activate the environment and configure a cloud provider. I've setup 
   AWS, but in principle you can use any provider that works with skypilot.
3. Launch your cluster using skypilot:
   ```bash
   sky launch -c fooocus launch-fooocus.yml
   ```
4. After the machine is provisioned, connect to the port using ssh port forwarding:
   ```bash
   ssh -L7860:localhost:7860 fooocus
   ```
5. Using your browser, connect to localhost:7860 and use the ui.
6. When you're done, remember to shut down the cluster.

