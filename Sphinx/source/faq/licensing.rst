.. _licensing:

.. role:: green
.. role:: orange

Can I use Orthanc in my commercial product?
===========================================

**Short answer:** yes, under certain conditions.

Orthanc's core has been released under the `GPL v.3 license <https://en.wikipedia.org/wiki/GNU_General_Public_License>`_ which means that, if anyone modifies Orthanc, integrates it in its product and **distributes** her product, she must make publicly available the source code of all Orthanc or derived work under a GPLv3 or more restrictive license (i.e AGPLv3).  

However, if the product is a SaaS application, the product is not **delivered** to the user and, in this case, she must not make the source publicly available.

Orthanc's plugins have been released under the `AGPL license <https://en.wikipedia.org/wiki/Affero_General_Public_License>`_ which is usually considered as **contaminating** license even when the product is not **delivered** (i.e a SaaS application).  As soon as Orthanc is used together with one of its AGPL plugin, Orthanc is contaminated by the AGPL and is considered AGPL herself.   If anyone writes a software that is part of the same process as an AGPL plugin, her software is contaminated by the AGPL license and she must make publicly available the source code of her software under an AGPLv3 or more restrictive license.


My commercial product interacts with Orthanc only through its Rest API or through DICOM
---------------------------------------------------------------------------------------

In this case, your product is not contaminated by Orthanc `GPL v.3 license <https://en.wikipedia.org/wiki/GNU_General_Public_License>`_ nor by any of the Orthanc's plugins `AGPL license <https://en.wikipedia.org/wiki/Affero_General_Public_License>`_.

I have written a plugin shall I make the code publicly available ?
----------------------------------------------------------------

If your plugin is the only one loaded by Orthanc, then, your plugin is only *contaminated* by Orthanc's GPL license.  Therefore, you'll need to make your plugin source code publicly available only if you **distribute** your software.

If another AGPL plugin is also loaded by Orthanc, then, your plugin is *contaminated* by the AGPL license and you must make the source code of your plugin publicly available.


Summary
-------

In all cases, you'll never be forced to make publicly available the parts of your product that is interacting with Orthanc only through the Rest API or through DICOM (Orthanc and it's AGPL plugins are not contaminating the *client* code).  

If, part of your product runs in the same process as Orthanc:

* I'm using only Orthanc and I don't modify it: :green:`no restrictions`

* I have modified Orthanc or written my own plugin and I'm not using any AGPL plugins: 

  * My product is accessible only as a SaaS (it is not distributed): :green:`no restricitons`
  * My product is distributed to my users (as a standalone application or as a server application my users can manage themselves): :orange:`You must make your Orthanc modifications and plugin publicly available`

* I'm using Orthanc and at least one AGPL plugin: :orange:`You must make your Orthanc modifications and plugins publicly available`


Note that, if you're not willing to make your code publicly available, there's an option to buy a licence exception. As for all open source projects, the intellectual propertly of Orthanc is still owned by multiple parties. In this case: CHU Liège University Hospital and Osimis S.A. The latter party, have the faculty to sell licence exceptions.

