**Resolved:** #Terraform #remote-exec #startup script

**Issue:** Not able to run the application app.py during provisioning
Removing '&' or running nohup not resolving the issue.
│ Error: execution halted
│ Error: remote-exec provisioner error

**Solution:**
As the best practice it is recommended to add the start in systemd services.
Same is achieved by adding app.py in systemd service and the application is started.
maint.tf is available in below github repo, this terraform file will add app.py in systemd and start the service as well.
