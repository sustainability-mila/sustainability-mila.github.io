---
layout: page-floatbutton
title: Donations
subtitle: We are looking forward to your donation!
permalink: /donate
---

We need your donation to support Ukrainian hospitals. Together we can provide cancer treatments and medical aid urgently needed to save lives in Ukraine.

# Donate now!

On our PayPal donation page you can donate from any country, with **debit card**, **credit card** or your **PayPal** account:

{% include donation-button.html %}

# Donations

We would like to raise {{ site.data.settings.donations.targetText}} CAD. Currently, we are working on a list of specific equipment and drugs requested by our Ukrainian partners (National Cancer Institute & local hospitals). We will publish the list here, as soon as it is finished. If you are part of pharma company that would like to donate drugs or equipment, please contact us (`{{ site.email }}`).

### Collected donations

{% include donation-bar-section.html %}

### Thank you!

A big thank you goes to everyone who supports us! Large donations from companies, small donations from students, equipment / drug donations from pharma - we are glad about every piece of help! Thank you for being here with us and standing up for Ukraine!

{% assign donors = site.data.donors %}
{% for donor in donors %}
{% include donor-card.html %}
{% endfor %}
