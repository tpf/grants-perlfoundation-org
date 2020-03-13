# Grant ideas for the TPF Grants.

People give us various grant ideas. If you are looking to spend some time to help the community and get some cash in return, 

Take a look at this list and give us a grant proposal. If you know an opportunity to improve Perl or Raku, you can [open an issue](https://github.com/tpf/grants-perlfoundation-org/issues) or [submit a pull request](https://github.com/tpf/grants-perlfoundation-org/pulls) and it will show up here.

While we try to keep this list relevant, things can easily get out of date. Before grabbing a task, check that a similar investment is not done recently.

⚠️ *Disclaimer* ⚠️ The list does not guarantee that TPF will fund these grant proposals.

# Perl

## Perl core

### [readpipe(LIST)](https://rjbs.manxome.org/rubric/entry/1964) (from @rjbs)

From the Perl todo:

> system() accepts a LIST syntax (and a PROGRAM LIST syntax) to avoid running a shell. readpipe() (the function behind qx//) could be similarly extended.


### [Unused lexicals](https://rjbs.manxome.org/rubric/entry/1964) (from @rjbs)

From the Perl todo:

This warns:

```bash
$ perl -we '$pie = 42'
  Name "main::pie" used only once: possible typo at -e line 1.
```

This does not:

```bash
$ perl -we 'my $pie = 42'
Logically all lexicals used only once should warn, if the user asks for warnings. An unworked RT ticket (#5087) has been open for eleven years for this discrepancy.
```

### [pack and unpack on streams](http://blogs.perl.org/users/makoto_nozaki/2015/07/grant-idea---pack-and-unpack-on-streams.html) (from @tux)

Currently, pack and unpack work on a string, which means that you have to move forward in the data-string yourself, if the full data-format is not known in advance, but depends on data seen so far.

If one could unpack on a stream, one could unpack the picture that is known, have the stream pointer move forward the amount of data read from the given picture, and be ready to read the next data based on a next, possibly different) picture.

Extreme “win” can be taken where the size of the data being read for a given picture is differing per architecture, like native floats.

## CPAN

### [PSGI protocol for HTTP::Tiny](https://perl-foundation-outreach.github.io/gsoc-2020-ideas/perl/HTTP-Tiny-PSGI.html)

Enhance HTTP::Tiny to support it communicating via PSGI. The primary use case being to assist in testing. See also LWP::Protocol::PSGI and Furl::PSGI.

### [Net::Google::Calendar authentication failure](https://rt.cpan.org/Public/Bug/Display.html?id=100421)

This library no longer works as it uses the Calendar v2 API which Google discontinued. It needs to be updated to the new API.

### [Module to handle OData](http://blogs.perl.org/users/makoto_nozaki/2015/07/grant-idea---odata.html) (from Alex aka ASB)

We (the Perl community) currently do not have a CPAN module that handles OData (cf. odata.org). There seems tob e an attempt to do it here: OData::Client But it's not finished yet, and i fit doesn't get a care taker, it will never be done. Also, there is client and server parts. Let's get both :)

Side node: Eventually, I'm too dumb to see that we don't need one because Perl can do it out oft he box. But if this is the case, eventuelly, it would be a good idea to put up a grant to create a document describing how to use OData with Perl (like this one)

## Tooling
### [Update PPI for more recent constructs](https://rjbs.manxome.org/rubric/entry/1964) (from @rjbs)

Last I looked, PPI couldn't handle much newer than Perl v5.10 or v5.12. I don't have a comprehensive list of the stuff it can't do, but it wouldn't be tiny. Make it all work.

## Documentation
### [DBIx::Class re-documentation](http://blogs.perl.org/users/makoto_nozaki/2015/07/grant-idea---dbixclass-re-documentation.html) (from @ribasushi)

> Fixing up the better-than-most-but-still-terrible documentation of DBIC is a ~200 person-hour undertaking, which on top of that requires someones fresh eye. Given that DBIx::Class is a "staple-module" in the contemporary Perl ecosystem, I believe it is reasonable to expect for the TPF to "pick up the tab" if someone with the right qualifications steps up.

## External site

### [BountySource has a few ideas on Perl.](https://www.bountysource.com/teams/perl/issues)

# Raku

## Raku core

## Raku ecosystem

## Tooling

## Documentation

### Document Red

Provide user documentation to the revolutionary Red ORM: https://github.com/FCO/Red

### Add code examples

Allow adding of notes (such as code examples) with the documentation, as is done on the PHP documentation site, e.g. https://www.php.net/manual/en/pcre.pattern.php

## Other areas of interest
