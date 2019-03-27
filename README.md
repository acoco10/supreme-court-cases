# JSON transcriptions of supreme court cases
The included case details and justice details were mostly compiled from oyez and wikipedia. Some corrections were made by hand.

The case files are saved in JSON in the form:
```javascript
// ~/Downloads/transcripts/2018/Apple_v._Pepper.js
{
    term: "2018",
    caseName: "Apple v. Pepper",
    caseLink: "https://www.oyez.org/cases/2018/17-204",
    caseTranscripts: [
        {
            transcriptTitle: "Oral Argument - November 26, 2018",
            transcriptLink: "https://apps.oyez.org/player/#/roberts10/oral_argument_audio/24778",
            transcript: [
                {
                    {
                        speakerName: "John G. Roberts, Jr.",
                        textObjs: [
                            {
                                text: "We'll hear argument first ...",
                                start: 0,
                                stop: 6.56,
                                duration: 6.56
                            }
                        ]
                    },
                    {
                        speakerName: "Daniel M. Wall",
                        textObjs:[
                            {
                                text: "Thank you, Mr. Chief Justice, ...",
                                start: 6.56,
                                stop: 46.8,
                                duration: 40.24
                            },
                            {
                                text: "Sample text ...",
                                start: 46.8,
                                stop: 56.8,
                                duration: 10.00
                            }
                        ]
                    }
                }
            ]
        }
    ]
}
```

An array of `caseTranscripts` is used to allow for cases that have more than one transcript as is the case with cases that lasted multiple days. `textObjs` is an array to allow for responses by individual speakers that are separated into separate paragraphs. As would be the case with:
> Daniel M. Wall
>
> Thank you, Mr. Chief Justice, and may it please the Court: The only damages theory in this monopolization action is rooted in a 30 percent commission that Apple charges app developers and which allegedly causes those developers to increase app prices to consumers.
>
> The case is barred by the Court's Illinois Brick doctrine because the developers' pricing decisions are necessarily in the causal chain that links the commission to any consumer damages. If the commission increases beyond the competitive level, but apps developers do not change their apps prices, consumers suffer no damages.