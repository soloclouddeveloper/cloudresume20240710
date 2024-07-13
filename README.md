## Project: cloudresume20240710
### Account: nativecloud.dev

#### TODO:
1. Terraform
    - storage bucket - public access
    - vpc
    - subnet
        - single region
        - CIDR /26 (/26 needed for proxy server IIRC)
        - stacktype: IPV4_ONLY
    - regional load balancer
    
2. Cloud Run
    - deploy FLASK webserver

## Required Services
`gcloud services enable [SERVICE]`

- compute.googleapis.com
    
## Roles and Permissions

Had to set compute.organizations.listAssociations at the org level.  Ref [reddit post: You don't have required permissions: compute.organizations.listAssociations to view the firewall policies inherited by this project. GCP](https://www.reddit.com/r/googlecloud/comments/15zuqvi/you_dont_have_required_permissions/)