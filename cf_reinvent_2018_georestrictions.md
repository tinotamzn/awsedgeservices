# CloudFront re:invent 2018 - Geo-restrictions

## Restricting the Geographic Distribution of Your Content

### Check that you have access to the content

1. Sign in to the AWS Management Console and open the CloudFront console at https://console.aws.amazon.com/cloudfront/
1. Search for the distribution without georestrictions (this distribution was autogenerated by the CFN templates and should have the ID **CFDIST03B** in the comments)
1. Copy the **Domain Name** and try to access to: *"https://{CFDomainName}/index.html"*
1. The HTTP response code should be **200 (Success)**

### To use the CloudFront console to add geo restriction to your CloudFront web distribution

1. Sign in to the AWS Management Console and open the CloudFront console at https://console.aws.amazon.com/cloudfront/
1. Search for the distribution without georestrictions (this distribution was autogenerated by the CFN templates and should have the ID **CFDIST03B** in the comments)
1. Click on the distribution, and then choose **Distribution Settings**
1. In the Distribution Settings pane, choose the **Restrictions** tab
1. Choose **Edit** and select **Yes** for **Enable Geo-Restriction**
1. Select **blacklist** and add **US - United States** to the blacklist
1. Choose **Yes, Edit**
1. Wait for the new configuration to be propagated

### Results

1. Since propagation takes ~10 minutes, a distribution with geographic restriction enabled was created as part of the CFN templates
1. Search for the distribution with georestrictions (this distribution was autogenerated by the CFN templates and should have the ID **CFDIST03A** in the comments)
1. Copy the **Domain Name** and try to access to: *"https://{CFDomainName}/index.html"*
1. The HTTP response code should be **403 (Forbidden)**