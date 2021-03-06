---
title: RDO test day Icehouse milestone 2
authors: ajeain, cmyster, eglynn, gszasz, kashyap, larsks, lon, nmagnezi, ohochman,
  panda, rbowen, rlandy, tkammer, tshefi, ukalifon, verdurin, whayutin, yeylon
wiki_title: RDO test day Icehouse milestone 2
wiki_revision_count: 35
wiki_last_updated: 2014-02-05
---

# RDO test day Icehouse milestone 2

We plan to hold a RDO test day on February 4th and 5th, 2014. This will be coordinated through the #rdo channel on Freenode, and through this wiki and the rdo-list mailing list.

We'll be testing the second Icehouse milestone release. If you can do any testing on your own ahead of time, that will help ensure that everyone isn't encountering the same problems.

## Who's Participating

* rbowen (Rich Bowen) - Test matrix, wiki stuff

* yeylon (Yaniv Eylon) - Foreman installation, IRC

* tshefi (Tzach Shefi) - GlusterFS semi distributed: Glance

* gfidente (Giulio Fidente) - GlusterFS semi distributed: Cinder

* gcerami (Gabriele Cerami) - Rhel6.5 VXLAN

* yrabl (Yogev Rabel) - Netapp semi distributed

* dron (Dafna Ron) - Netapp semi distributed

* nlevinki (Nathan Levinkind) - Local TGT semi distributed

* nmagnezi (Nir Magnezi) - Neutron ML2, Neutron OVS

* larsks (Lars Kellogg-Stedman) - IRC

-kashyap (Kashyap Chamarthy) - IRC; Libvirt/QEMU/KVM/

* ajeain (Ami Jeain) - Horizon

* augol/cmyster (Amit Ugol) - Heat

* ukalifon (Udi Kalifon) - Keystone

* ohochman (Omri Hochman) - Foremen, Nova - IRC

* gszasz (Gabriel Szasz) - Nova, IRC

* rlandy (Ronelle Landy) - Tripleo/Tuskar

* weshay ( Wes Hayutin ) - Packstack

* eglynn (Eoghan Glynn) - Ceilometer

* tkammer (Tal Kammer) - Foremen installation - IRC

* verdurin (Adam Huffman) - Packstack, CentOS

* lon (Lon Hohberger) - EL7-specific installation, general testing

## Prerequisites

We plan to have have packages for the following platforms:

*   Fedora 20
*   RHEL 6.5
*   RHEL 7 beta
*   CentOS 6
*   CentOS 6.5

You'll want a fresh install with latest updates installed. (Fresh so that there's no hard-to-reproduce interactions with other things.)

## How To Test

    sudo yum install http://rdo.fedorapeople.org/openstack-icehouse/rdo-release-icehouse.rpm

*   Check for any [ Workarounds](Workarounds_2014_02) required for your platform before the main installation
*   For Packstack based deployment start at step 2 of -- <http://rdoproject.org/Quickstart#Step_2:_Install_Packstack_Installer>
*   For Foreman based deployment on RHEL & its derivatives, -- <http://rdoproject.org/Virtualized_Foreman_Dev_Setup>

### Test cases and results

The things that should be tested are listed on the [Tested Setups](TestedSetups_2014_02) page.

*   Pick an item from the list
*   Go through the scenario as though you were a beginner, just following the instructions. (Check the [ Workarounds](Workarounds_2014_01) page for problems that others may have encountered and resolved.)
*   KEEP GOOD NOTES. You can use <https://etherpad.openstack.org/p/rdo_test_day_feb_2014> for these notes. Reviewing other peoples' notes may help you avoid problems that they've already encountered.
*   Compare your results to the CI results @ <https://prod-rdojenkins.rhcloud.com/>
*   Execute the openstack test suite tempest @ [Testing IceHouse using Tempest](Testing IceHouse using Tempest)

If you have problems with any of the tests, report a bug to [Bugzilla](https://bugzilla.redhat.com) usually for one of the [openstack-packstack](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-packstack), [openstack-nova](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-nova), [openstack-glance](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-glance), [openstack-keystone](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-keystone), [openstack-cinder](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-cinder), [openstack-neutron](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-neutron), [openstack-swift](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-swift), [python-django-horizon](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=python-django-horizon), [openstack-heat](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-heat) or [openstack-ceilometer](https://bugzilla.redhat.com/enter_bug.cgi?product=RDO&version=18&component=openstack-ceilometer) components. If you are unsure about exactly how to file the report or what other information to include, just ask on IRC (#rdo, freenode.net) and we will help you.

Once you have completed the tests, add your results to the table on the [TestedSetups](TestedSetups_2014_02) page, following the examples already there. Be sure to check the [ Workarounds](Workarounds_2014_01) page for things that may have already have fixes or workarounds.
