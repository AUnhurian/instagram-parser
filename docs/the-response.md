# The response objects

## Instagram Post object
Once you run the tags parser in your console, you will get an infinite bunch of
objects similar to this one:

```php
Mineur\InstagramParser\Model\InstagramPost {#36
  -id: 1539101913268979330
  -comment: """
    ¡Disfruta del sol pero sin quemarte! #wearsunscream #cremasolar
    """
  -commentsCount: 0
  -shortCode: "BVb_QkdhaC"
  -takenAtTimestamp: "149769267"
  -dimensions: Mineur\InstagramParser\Model\MediaDimensions {#31
    -height: 1079
    -width: 1080
  }
  -likesCount: 21
  -mediaSrc: "https://scontent-mrs1-1.cdnins/672_n.jpg"
  -thumbnailSrc: "https://cdninstagr.am/84672_n.jpg"
  -ownerId: "1103553924"
  -video: false
  -commentsDisabled: false
}
```

## User object
Once you run the parser you will get a Uer object like this one:
```php
Mineur\InstagramParser\Model\User {#33
  -id: "182889088"
  -username: "alexcm14"
  -fullName: "Alex Casajuana"
  -biography: "Software craftsman apprentice"
  -follows: 19
  -followedBy: 12
  -externalUrl: null
  -countryBlock: false
  -isPrivate: false
  -isVerified: true
  -profilePictureUrl: "https://insta.gram.net/t870_a.jpg"
  -profilePictureUrlHd: "https://insta.gram.net/t8x70_a.jpg"
  -connectedFacebookPage: null
  -media: array:12 [
      // user media array
  ]
```