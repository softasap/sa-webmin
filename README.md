sa-webmin
=========

[![Build Status](https://travis-ci.com/softasap/sa_webmin.svg?branch=master)](https://travis-ci.com/softasap/sa_webmin)
[![Build Status](https://github.com/softasap/sa_webmin/workflows/CI/badge.svg?event=push)](https://github.com/softasap/sa_webmin/actions?query=workflow%3ACI)

Example of usage:

Simple

```YAML

     - {
         role: "sa_webmin"
       }


```

Advanced

```YAML


     - {
         role: "sa_webmin",
         webmin_listen: 10000,
         webmin_port: 10000,
         webmin_use_ssl: 0,
         # override some custom params in /etc/webmin/miniserv.conf    
         # that differs from params above
         webmin_miniserv_properties_extra:
              - {
                  regexp: "^ssl=.*$",
                  line: "ssl={{ webmin_use_ssl }}"
                }

```



Usage with ansible galaxy workflow
----------------------------------

If you installed the `sa_webmin` role using the command


`
   ansible-galaxy install softasap.sa_webmin
`

the role will be available in the folder `library/softasap.sa_webmin`
Please adjust the path accordingly.

```YAML

     - {
         role: "softasap.sa_webmin"
       }

```




Copyright and license
---------------------

Code is dual licensed under the [BSD 3 clause] (https://opensource.org/licenses/BSD-3-Clause) and the [MIT License] (http://opensource.org/licenses/MIT). Choose the one that suits you best.

Reach us:

Subscribe for roles updates at [FB] (https://www.facebook.com/SoftAsap/)

Join gitter discussion channel at [Gitter](https://gitter.im/softasap)

Discover other roles at  http://www.softasap.com/roles/registry_generated.html

visit our blog at http://www.softasap.com/blog/archive.html 
