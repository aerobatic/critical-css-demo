# Critical CSS Optimization Demo

This [Aerobatic](https://www.aerobatic.com) demo site showcases the performance improvements offered by the [critical css inline optimization](https://www.aerobatic.com/docs/site-optimization/#critical-css-inlining). The site was generated using the [Bootstrap Agency](http://startbootstrap.com/template-overviews/agency/) quick start.

~~~sh
aero create --quick-start html5/sb-agency
~~~

There are two versions of the site - with and without the critical CSS inlining optimization enabled. The [aerobatic.yml](/blob/master/aerobatic.yml) contains the following configuration:

~~~yaml
deploy:
  optimizer:
    inlineCriticalCss: true
~~~

### Results

The [Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights) tool was run against each version. The improvement is particularly significant on mobile devices.

Mode | URL | Desktop Score | Mobile Score | PageSpeed Results |
---|---|---|---|---
**Without** critical CSS inlining | https://critical-css-demo.aerobatic.io/ | 90 / 100 | 74 / 100 | [View Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fcritical-css-demo.aerobatic.io%2F)
**With** critical CSS inlining | https://critical-css-demo--optimized.aerobatic.io | **98** / 100 | **98** / 100 | [View Results](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fcritical-css-demo--optimized.aerobatic.io%2F)
