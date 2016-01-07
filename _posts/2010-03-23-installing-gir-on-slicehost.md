---
layout: post
title: Installing Ægir on Slicehost
created: 1269353885
categories: []
---
<p><a href="http://drupalcode.org/viewvc/drupal/contributions/profiles/hostmaster/INSTALL.txt?revision=DRUPAL-6--0-3&view=co">Documentation</a>.</p>
<p>Problems and solutions</p>

<p>Running commands such as</p>
<code>$DRUSH dl provision --destination=.drush</code>
<p>did not work, but adding php at the beginning of the command did:</p>
<code>php $DRUSH dl provision --destination=.drush</code>

<li>"<Directory /var/aegir/drupal-6.16>" and "DocumentRoot /var/aegir/drupal-6.16" in ./config/vhost.d/$AEGIR_DOMAIN</li>
