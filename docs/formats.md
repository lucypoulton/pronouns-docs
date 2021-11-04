# Formats

The English language is a pain. I've tried to make this a simple as possible to understand, but sadly computers are 
awful at interpreting complex and often ambiguous language, so it's a little complicated.

## The canonical format

Every pronoun set that the plugin uses has a canonical format. Even if you don't see or interact with it, every set has
one of these, either hardcoded into the plugin, the config or the cloud database. It looks like this:
##### subjective/objective/progressive/possessive adjective/possessive pronoun/reflexive

##### Subjective
**They** will do it if you ask nicely.

##### Objective
I'd really love to get to know **them**.

##### Progressive
**They're** a very cool person.

(This isn't actually a pronoun, instead being a contraction of the subjective and conjugated verb "to be". 
It's just helpful to have.)

##### Possessive adjective
I hope **their** day is going well.
##### Possessive pronoun
Whose is that? Oh, it's **theirs**.
##### Reflexive
This person should be really proud of **themself**.

Writing out the canonical format can be a little confusing, so [I wrote a webpage](https://pn.lucypoulton.net/add) as 
part of the cloud to simplify it. Complete the sentences by filling out the boxes and it'll do the rest for you.

## Setting your pronouns

(if you're here from a plugin help link, welcome!)

Fortunately, with common pronouns you don't have to worry about the canonical format - the plugin will try its best to
match anything with a set. 

For example, `she`, `they`, `he/him`, `they/fae/she` and `any` are all understood by the plugin just fine.

There are situations where the plugin has multiple sets to choose from, for example `xe`. At the time of writing, the
database contains two variations on this set, `xe/xem/xe’s/xyr/xyrs/xemself` and `xe/xer/xe's/xer/xers/xerself`. It will
pick one at random to use and inform you that it couldn't figure out which one you wanted. In this case, add more pronouns
on the end until it's no longer ambiguous, or use the canonical format.