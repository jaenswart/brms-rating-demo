JBoss BRMS 6 Rating Demo
=========================
Project to automate the installation of this product without preconfiguration beyond a single admin user.

There are four options available to you for using this demo; local, Openshift Online, Red Hat CDK OpenShift Enterprise and
Containerized.


Option 1 - Install on your machine
----------------------------------
1. [Download and unzip.](https://github.com/jbossdemocentral/brms-rating-demo/archive/master.zip)

2. Add product installer to installs directory.

3. Run 'init.sh' or 'init.bat' file. 'init.bat' must be run with Administrative privileges

4. Login to http://localhost:8080/business-central  (u:erics / p:jbossbrms1!)

5. Enjoy installed and configured JBoss BRMS 6.


Option 2 - Install with one click in xPaaS (brmsPaaS)
-----------------------------------------------------
After clicking button, ensure `Gear` size is set to `large`:

[![Click to install OpenShift](http://launch-shifter.rhcloud.com/launch/light/Install brmsPaaS.svg)](https://openshift.redhat.com/app/console/application_type/custom?&cartridges[]=https://raw.githubusercontent.com/jbossdemocentral/cartridge-brmsPaaS/master/metadata/manifest.yml&name=brmspaas&gear_profile=large&initial_git_url=)

Once installed you can use the JBoss BRMS logins:

   * u:erics  p: jbossbrms  (admin)

   * u: alan  p: jbossbrms  (analyst)

Current hosting of bpmPaaS is on JBoss BRMS 6.0.2 in OpenShift Online.


Option 3 - Install on Red Hat CDK OpenShift Enterprise image
------------------------------------------------------------
The following steps can be used to install this demo on OpenShift Enterprise using the
Red Hat Container Development Kit (CDK)

1. [App Dev Cloud with JBoss BRMS Rating Demo](https://github.com/redhatdemocentral/rhcs-brms-rating-demo)


Option 4 - Generate containerized install
-----------------------------------------
The following steps can be used to configure and run the demo in a container

1. [Download and unzip.](https://github.com/jbossdemocentral/bpms-rating-demo/archive/master.zip)

2. Add product installer to installs directory.

3. Copy contents of support/docker directory to the project root.

4. Build demo image

	```
	docker build -t jbossdemocentral/brms-rating-demo .
	```
5. Start demo container

	```
	docker run -it -p 8080:8080 -p 9990:9990 jbossdemocentral/brms-rating-demo
	```
6. Login to http://&lt;DOCKER_HOST&gt;:8080/business-central  (u:erics / p:jbossbrms1!)

7. Enjoy installed and configured JBoss BRMS 6.

Additional information can be found in the jbossdemocentral container [developer repository](https://github.com/jbossdemocentral/docker-developer)




![JBoss BRMS](https://github.com/jbossdemocentral/brms-rating-demo/blob/master/support/jboss-brms.png?raw=true)
