## from version "piazza-20132010181251": ##

Team Piazza supports Gravatar.com user pictures. Just leave the field "Your image URL" empty and the users email address is used to get the users Gravatar image.


## from version "piazza-201110241711": ##

Every user can now configure his portrait on his configuration page under "My Settings & Tools".

Piazza determines who is responsible for a commit by looking at the committers and nicknames within the commit message. You can configure the nicknames of a user under "Version Control Username Settings".

![http://team-piazza.googlecode.com/svn/wiki/piazza_configure_portrait.png](http://team-piazza.googlecode.com/svn/wiki/piazza_configure_portrait.png)

The xml config is no longer supported.




## team-piazza prior to version "piazza-201110241711" ##

Piazza displays the portraits of the programmers responsible for a build.  It determines who is responsible by looking for nicknames the commit comments.  This means that programmers must identify who worked on a commit in the commit message when they check their changes into source control.  This feature encourages programmers to write good commit messages and, if pair programming. identify both members of the pair responsible for every change.

A Piazza-compatible commit message looks something like:

```
Alice and bob added Javascript animation effects to the web front-end
```

If suitably configured, Piazza will then show the portraits of Alice and Bob while Team City builds and tests their changes.

Piazza reads the mapping of nicknames to portraits from the Team City server's `$HOME/.BuildServer/config/main-config.xml` configuation file.

```
<?xml version="1.0" encoding="UTF-8"?>
<server rootURL="...">
  ...
  <piazza>
    <user portrait="http://www.example.com/alice.png">
      <name>Alice Band</name>
      <nickname>alice</nickname>
      <nickname>aband</nickname>
    </user>
    <user portrait="http://www.example.com/bob.png">
      <name>Bob Frapples</name>
      <nickname>bob</nickname>
      <nickname>rob</nickname>
      <nickname>bfrapples</nickname>
    </user>
  </piazza>
</server>
```

The configuration for Team Piazza is in an element called "piazza" that is an immediate child of the root element ("server").  The "piazza" element contains one or more "user" elements that each defines the name, portrait URL and nicknames of a user.