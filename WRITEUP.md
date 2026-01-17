# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
APP Service:
  13/month with B1 Basic includes storage and networking. costs are low. No VM or dedicate disks 
  App can scale between tiers B1 -> S1 -> P1v3, etc
  Auto-scale 
  Managed platform with built in health monitoring 
  simple deployment with integrated github actions, CI/CD, logging/log stream

VM:
  B1 is around 20-40 a month
  has managed sisks premium ssd/hdd
  public ip cost
  running small VM cost more than app service
  vertical scaling with much more manual work
  manual os updates, manual setup, manual process management. 

I chose app service because it was cheaper and easier. VM almost made me cry. impossible if you are not familiar with limux configuration. i had to do everything manually. 
app service is more scalable 
also better integration with MSL and looging


FInal verdict
App Service → Best for this CMS: low cost, high availability, easy scaling, simple workflow.
VM → Only needed for workloads requiring full OS control, custom binaries, or special networking.
