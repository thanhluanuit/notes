# Performance Optimization Checklist

## Frontend

1. Make Fewer HTTP Requests
2. Put Stylesheets at the Top 
3. Put Scripts at the Bottom
4. CSS Sprite
5. Load Asynchronous Scripts file
6. Optimize Images:
    - Compress image
    - Resize image
    - Load progressive
    - Size specific, don’t scale


## Backend

1. Database
    - Indexes
    - Avoid (N+1) query
    - Batch loading
    - Transaction 

2. Caching:
    - Fragment caching
    - Query caching
    - Redis caching

3. Run big process in background jobs

4. Use DNS: To serve images, assets (Sharding Dominant Domains)

5. Upgrade Rails, update gems, reduce gem.


## Server (Nginx or Apache)
1. Add an Expires Header
2. Gzip Components
3. Using Proxy to Cache on Nginx
4. Config Worker
5. HTTP2


## Tools for monitor
- New Relic
- Pingdom


## Tools for measure performance
- PageSpeed Insight: https://developers.google.com/speed/pagespeed/insights
- GTmetrix: https://gtmetrix.com
- WebPageTest: https://www.webpagetest.org
- Pingdom: https://www.pingdom.com


## Resources
- Book: 
    - High Performance Web Sites
    - Even Faster Web Sites: Performance Best Practices for Web Developers 
- PageSpeed Insights Rules: https://developers.google.com/speed/docs/insights/rules
- Best Practices for Speeding Up Your Web Site: https://developer.yahoo.com/performance/rules.html
- Tuning NGINX for Performance: https://www.nginx.com/blog/tuning-nginx/
- 5 Tips to Speed up Your Website: http://luanotes.com/posts/5-tips-to-speed-up-your-website
- Frontend performance checklist: https://www.smashingmagazine.com/2018/01/front-end-performance-checklist-2018-pdf-pages/
- Progressive image loading: https://blog.botreetechnologies.com/page-load-optimization-by-progressive-image-loading-like-medium-1d0f94744a4d
- https://www.railsspeed.com
- https://www.speedshop.co/blog
