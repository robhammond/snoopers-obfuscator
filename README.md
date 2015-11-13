# Snooper's Obfuscator

The UK Government's [Investigatory Powers bill](http://www.theguardian.com/world/2015/nov/04/investigatory-powers-bill-the-key-points) proposes that internet service providers should be compelled to keep a record of every website every person in the UK visits.

The Home Secretary [Theresa May has said](https://www.gov.uk/government/speeches/home-secretary-publication-of-draft-investigatory-powers-bill) this is "simply the modern equivalent of an itemised phone bill."

It is not. It is [so much more](http://www.theguardian.com/commentisfree/2015/nov/10/frankie-boyle-theresa-may-internet-surveillance).

## Security through obscurity

Internet users in the UK should have the right to protection against intrusive government surveillance.

This script aims to provide a little security to UK internet users by:

1. Obscuring your actual browsing habits by adding a constant 'random surfer' to your home
2. Place more burdens on the practicality of the legislation by filling up logs with useless information

It does this constantly requests random websites from Quantcast's [top websites list](https://www.quantcast.com/top-sites), or performs a random Google search, and then clicks on a random number of links from the websites it finds.

## Install

Install Perl >= 5.10, and these modules:

* Mojolicious
* Modern::Perl

Then to run in the background:

`nohup perl obfuscate.pl 2>1 &`

The script runs in an infinite loop but it's possible it could encounter an error and stop, so you may want to write a shell script & cron job to ensure it keeps running.