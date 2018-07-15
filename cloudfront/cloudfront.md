## CloudFront

Cloudfront is amazon's content delivery network. A content delivery network is a system of distributed servers(network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage and the content delivery server. Content is actually served from edge locations in case of cloudfront. Its the place where data is cached and served to nearby areas. 

Terms:
- Edge locations
- Origin: the origin is the place where our original files actually are. This can be either of 4 things: s3 bucket, ec2 instance, elastic load balancer or route53
- Distribution: This is the name given to the cdn that consists of a collection of edge locations. There can be 2 different types of distributions:
    - web: typically used for websites
    - RTMP: media streaming

How a CDN works:
Lets say we have our content(may be static content) stored in an s3 bucket in the london region. Lets we have a couple of users in australia are requesting content from that bucket. For the first user who requests it, the request is actually going to go to the edge location in australia, if the content is not found, it is going to be fetched from the s3 bucket. The content that is fetched will have a TTL(time to live) associated with it which defines the time that the content will live in the edge location. For the second user who requests for the same content, the request will be served from the edge location and not the original s3 bucket(orgin) as it had been cached previously in the edge location. If the TTL expires, the content will be again fetched from the bucket if a new user requests it.

It is totally possible to write into an edge location as well. Objects in an edge location are cached for the life of the TTL(time to live) after they are deleted. However one thing to note is that it is totally possible to clear the cache manually too however customers are charged for that.
