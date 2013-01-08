xml2json
========

Javascript library that convert XML into a  JSON object


## Example

*Input:*

```xml
<ALEXA VER="0.9" URL="davidwalsh.name/" HOME="0" AID="=">
  <SD TITLE="A" FLAGS="" HOST="davidwalsh.name">
    <TITLE TEXT="David Walsh Blog :: PHP, MySQL, CSS, Javascript, MooTools, and Everything Else"/>
    <LINKSIN NUM="1102"/>
    <SPEED TEXT="1421" PCT="51"/>
  </SD>
  <SD>
    <POPULARITY URL="davidwalsh.name/" TEXT="7131"/>
    <REACH RANK="5952"/>
    <RANK DELTA="-1648"/>
  </SD>
</ALEXA>
```

*output:*

```json
{
  "@attributes": {
    AID: "=",
    HOME:  0,
    URL: "davidwalsh.name/",
    VER: "0.9",
  },
  SD = [
    {
      "@attributes": {
        FLAGS: "",
        HOST: "davidwalsh.name",
        TITLE: A
      },
      LINKSIN: {
        "@attributes": {
          NUM: 1102
        }
      },
      SPEED: {
        "@attributes": {
          PCT: 51,
          TEXT: 1421
        }
      },
      TITLE: {
        "@attributes": {
          TEXT: "David Walsh Blog :: PHP, MySQL, CSS, Javascript, MooTools, and Everything Else",
        }
      },
    },
    {
      POPULARITY: {
        "@attributes": {
          TEXT: 7131,
          URL: "davidwalsh.name/"
        }
      },
      RANK: {
        "@attributes": {
          DELTA: "-1648"
        }
      },
      REACH: {
        "@attributes": {
          RANK = 5952
        }
      }
    }
  ]
}
```
