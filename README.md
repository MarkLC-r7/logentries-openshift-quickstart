Logentries on OpenShift
======================

This git repo provides a quick method to get your OpenShift logs streaming to Logentries.

Running on OpenShift
----------------------------

Create a Logentries account at https://logentries.com/doc/openshift/

Create an application on Openshift if you havent already, you must enter app name and your stack.  Change directories into the resulting application directory.

        rhc app create myappname mystack --from-code https://github.com/openshift/logentries-openshift-quickstart
        cd myappname

Configuration
-------------

Configure logentries/le_config.ini file with your Logentries Account Key

To obtain this, you need to log-in to your Logentries account and click Account in the left sidebar, then click the Account Key button
and copy the value you are given.

Paste this inside the quotation marks in logentries/le_config.ini

Then push the repo

	git add .
	git commit -m "my first commit"
	git push

That's it, you can now check your logs, by logging into your Logentries account or refreshing the page.
