![screenshot](pics/fish.jpeg)

Ever woken up in the middle of the night with a cold sweat, because you realized you may have accidently commited those credentials? Now you know how i feel.

Developers are human we make mistakes, sometimes even in a completely zero-trust environment accidents still happen. That is why I like to design platforms that are Stupid proof especially when protecting sensitive data.

So you have all the checks for.a zero-trust environment and you are doing token and session based temporary access everywhere. (RBAC + SSO)

There are still one tiny cracks and that is that resources use roles can generate credentials either through the AWS SDK, via an instance profile or via the metadata service.

```python
import boto3
```

So how do you overcome this hurdle while still giving the developers the flexibility they need? Introducing AWS RCPs no longer do you have to attach clunky unmanageable deny policies to each of your roles. But rather now you can create a resource policy to deny all traffic that is not coming from your private VPC.

AccessDenied 


