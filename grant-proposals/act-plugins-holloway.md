# Grant Proposal: New payment plugins and testing tools for Act

## Grantee: D Ruth Holloway

## Synopsis

[Act](https://act.mongueurs.net), a conference toolkit, has worked well for many years over numerous conferences. It was formerly the prime choice of conference management toolkit for Perl conference globally. In recent years, the TPRF has moved away from it to fragmented solutions, many of which cost a lot more money than the value they gave the community. In 2026, the conference team and Board have suggested moving TPRC 2027 to Act.

Payment-processors have been integrated with Act over the years, including [PayPal](https://paypal.com) and [CyberMut from Crédit Mutuel](https://www.creditmutuel.fr/home/index.html). It would be useful to TPRF for payment plugins to be available for Stripe and/or Square, and Act can also be improved and modernized with additional testing tools for existing plugins, to ensure that breaking API changes at the various payment vendors are caught quickly.

## Grant Deliverables

* An Act payment plugin for [Square](https://squareup.com).
* An Act payment plugin for [Stripe](https://stripe.com).
* Unit and functional tests for the new plugins, plus all existing plugins, that will catch breaking API changes from either Act or from the payment vendors.
* Updated documentation for the payment plugin base class and all existing plugins.

## Timetable

[Les Mongueurs de Perl](https://mongueurs.net), which hosts and supports Act, is planning a major upgrade and modernization before the end of 2026, including bringing the system up to use PSGI rather than mod_perl, and also planning to move to new hardware. The deliverables for this grant could not be merged prior to that upgrade; however, with the Payments plugin API not planned for changes, the grantee may begin work on the payments side of the equation, and save a final check for after the upgrade. Expect completion, in December 2026 or January 2027, in plenty of time for ticket sales for the 2027 TPRC in Waterloo, Ontario, Canada.

## About the Grantee

D Ruth Holloway has been a Perl monger for over 25 years, starting with reporting and data manipulation tasks for libararies in 2001, and steady growth to full-stack implementations of large-data-scale business process automations. She is a [CPAN author](https://metacpan.org/author/GEEKRUTH) and a member of the [Dancer](https://metacpan.org/pod/Dancer2) Core Team, where she has specialized in writing and maintaining numerous plugins in the ecosystem. She has written numerous REST-API-based plugins for systems she has been working on outside the Dancer space, as well.

## Grant Amount

The grant is proposed for USD \$2000.00, payable in two payments of USD \$1000.00: one after grant approval, and one after completion has been certified by the Grant Manager.

## Proposed Grant Manager

The grantee proposes Philippe Bruhat [BooK](https://metacpan.org/author/BOOK) as the Grant Manager for this grant; he is the lead maintainer of the master repository for Act [on GitHub](https://github.com/book/act), and heavily involved in the planned upgrade. 
