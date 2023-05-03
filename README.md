# Diplomacy
Resources for when I actually build this out– useful assets for an online version of the diplomacy board game with a visual order entry UI on the map.

---

`diplomacy.svg` has been hand annotated with elements id's corresponding to key locations:

army/fleet unit placement points (example):

```
<g id="A_CLY">
<circle cx="320" cy="377" r="2" fill="#BAB4AB" fill-opacity="0.43"/>
<circle cx="320" cy="377" r="1.5" stroke="#3D3A37" stroke-opacity="0.53"/>
</g>
<g id="A_EDI">
<circle cx="354" cy="338" r="2" fill="#BAB4AB" fill-opacity="0.43"/>
<circle cx="354" cy="338" r="1.5" stroke="#3D3A37" stroke-opacity="0.53"/>
</g>
<g id="A_TUN">
<circle cx="448" cy="939" r="2" fill="#BAB4AB" fill-opacity="0.43"/>
<circle cx="448" cy="939" r="1.5" stroke="#3D3A37" stroke-opacity="0.53"/>
</g>
<g id="F_NAF">
<circle cx="351" cy="890" r="2" fill="#22457A" fill-opacity="0.43"/>
<circle cx="351" cy="890" r="1.5" stroke="#22457A" stroke-opacity="0.53"/>
</g>
<g id="F_SPA:SC">
<circle cx="259" cy="815" r="2" fill="#22457A" fill-opacity="0.43"/>
<circle cx="259" cy="815" r="1.5" stroke="#22457A" stroke-opacity="0.53"/>
</g>
<g id="F_SPA:NC">
<circle cx="168" cy="646" r="2" fill="#22457A" fill-opacity="0.43"/>
<circle cx="168" cy="646" r="1.5" stroke="#22457A" stroke-opacity="0.53"/>
</g>
```

supply center points (example):

```
<g id="PAR_SC" clip-path="url(#clip3_0_1)">
<path... /> ...
</g>
<g id="BRE_SC" clip-path="url(#clip4_0_1)">
<path... /> ...
</g>
<g id="ROM_SC" clip-path="url(#clip5_0_1)">
<path... /> ...
</g>
```

regions (for shading ownership):

```
<g id="SPA_REGION" ... </g>
....
<g id="HOL_REGION" ... </g>
....
<g id="NAF_REGION" ... </g>
```

PNG files for fleet units, army units, supply centers, & flags are in `/icons`– center them on their respective points in the SVG using the ID's.

`diplomacy.json` contains all valid army + fleet movements from any space to another. Note that there is a minor discrepancy with the map for `BUL:NC`, which is drawn as `North Coast` but usually `East Coast`. If the `abbreviations` property is used well this can be easily dealt with.

Add a transparent layer on top of the map in the app for order markers and interactivity.

Don't have time to finish this project right now so feel free to use any of this to bootstrap your own.

Note that Diplomacy has quite a few corner cases when adjudicating orders and you really won't want to rebuild the wheel– wrapping this will speed things up https://github.com/diplomacy/diplomacy.
