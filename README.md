# Baseball Pitch Caller

This tool was inspiried by playing online games in [MLB the Show](https://theshow.com/). It is easy to fall into predicitable patterns when pitching over multiple innings. Pitchers want to keep hitters guessing. If they always throw the same pitch in the same situation, hitters will figure it out. So, this tool uses stochastic sampling to introduce randomness in a smart way.

[Try the tool now &raquo;](https://kowalike.github.io/baseball-pitch-caller/)

## How does stochastic sampling fit in?

Imagine a pitcher has a “menu” of pitches: fastball, slider, curveball, changeup. Instead of deciding pitches in a fixed pattern (like fastball every first pitch), the pitcher uses probabilities. For example:

- Fastball: 50%
- Slider: 30%
- Curveball: 15%
- Changeup: 5%

When it’s time to throw, the tool randomly picks a pitch based on those probabilities. That’s stochastic sampling — random, but weighted by strategy.

## Why not pure randomness?

If you just roll dice with equal chances, you might throw too many curveballs or too few fastballs. Weighted randomness ensures:

- You stick to your overall game plan.
- You stay unpredictable to the hitter.

## How it works

Instead of always picking the single “best” pitch, the tool uses a technique called softmax sampling (a form of stochastic sampling) to turn factors like the pitcher’s handedness, the batter’s side, the selected pitch mix, the current count, and the batter’s swing timing into probabilities and then randomly selects a pitch and location based on those probabilities. This means the choices aren’t completely random — they’re weighted toward smarter options — but they’re not predictable either.

[Try the tool now &raquo;](https://kowalike.github.io/baseball-pitch-caller/)

1. Adjust the Stochastic Sampling temperature slider to how “wild” or “safe” the recommendations are.
2. Select the pitcher's handedness.
3. Select the the pitcher's arsenal (chose between 3 and 5 pitches).
4. Select which side the batter is hitting from (left side or right side).
5. Click the "Suggest Initial Pitch & Location" button to generate the first pitch of the sequence.
6. Execute the pitch, then report whether the pitch was a ball or strike and the swing timing.
7. After an at bat has ended, click the "Suggest Next Pitch and Location" button to begin a new sequence.

You can also export the session as a JSON file if you would like to perform further analysis.

## Contributing

Contributions are welcomed and encouraged. Please feel free to expand and improve on the original code and add your contributions to the project.
