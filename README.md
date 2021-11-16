# Object Notation

Say we have an object called `seasonConfig`, it looks like this:
```javascript
const seasonConfig = {
  summer: {
    text: 'Lets hit the beach!',
    iconName: 'sun'
  },
  winter: {
    text: 'brrr it's cold',
    iconName: 'snowflake'
  }
};
```

So if you wanted the `text` and `iconName` for `summer`. You can do this:
```javascript
const text = seasonConfig.summer.text;
const iconName = seasonConfig.summer.iconName;
```

There's another way to do this though, the below will do the _exact same thing_, create an `text` and `iconName` variable:
```javascript
const { text, iconName } = seasonConfig.summer;
```

Now, there's another way we can write `seasonConfig.summer`, and it's like this: `seasonConfig["summer"]`. BOTH of these things are the SAME THING. If you can see where we're going with this, the `season` variable you have should be either `"summer"` or `"winter"`. Building on the above example, we should be able to write:
```javascript
const { text, iconName } = seasonConfig[season];
```
