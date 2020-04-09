# mplsoccer

mplsoccer is a Python plotting library for drawing soccer / football pitches quickly in Matplotlib. It also contains a module to load StatsBomb open-data.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install mplsoccer.

```bash
pip install mplsoccer
```

## Pitch plotting basics

TO DO

mplsoccer can either plot on existing axis or create new axis.

#### Pitch type
mplsoccer currently supports several data formats:
- Statsbomb
- Stats Perform
- Tracab (ChyronHego) tracking data
- Opta
- STATS (formerly Prozone)
- Wyscout (the pitch dimensions are taken from ggsoccer: https://github.com/Torvaney/ggsoccer)

The following example draws a Statsbomb pitch (the default) with stripes.
``` python
from mplsoccer.pitch import Pitch
pitch = Pitch(orientation='horizontal',figsize=(10,10),stripe=True)
fig, ax = pitch.draw()
fig.savefig('statsbomb.png',pad_inches=0,bbox_inches='tight')
```
![alt text](https://github.com/andrewRowlinson/mplsoccer/blob/master/docs/figures/README_example_statsbomb_pitch.png?raw=true "statsbomb pitch")

For fun you can also plot the same pitch in xkcd mode.
``` python
from mplsoccer.pitch import Pitch
import matplotlib.pyplot as plt
plt.xkcd()
pitch = Pitch(orientation='horizontal',figsize=(10,10),stripe=True)
fig, ax = pitch.draw()
fig.savefig('statsbomb_xkcd.png',pad_inches=0,bbox_inches='tight')
```
![alt text](https://github.com/andrewRowlinson/mplsoccer/blob/master/docs/figures/README_example_xkcd_pitch.png?raw=true "pitch xkcd style")

#### Views

#### Layout
- figsize
- layout

#### Appearance

#### Padding

#### Axis


## StatsBomb open-data

TO DO


## Plotting

TO DO

###### 1. Plot

###### 2. Scatter

###### 3. Lines

###### 4. Arrows

###### 5. Kdeplot

###### 6. Jointplot

###### 7. Hexbin

###### 8. Heatmap

###### 9. Annotation

###### 10. Animation

###### 11. Advanced examples

## Inspiration

mplsoccer was inspired and built on others work:
- [Peter McKeever](http://petermckeever.com/2019/01/plotting-pitches-in-python/) inspired the API design
- [ggsoccer](https://github.com/Torvaney/ggsoccer) - library for plotting pitches in R
- [lastrow](https://twitter.com/lastrowview) - often tweets animations from matches and the code
- [fcrstats](http://fcrstats.com/) - tutorials in using football data
- [Karun Singh](https://twitter.com/karun1710) - interesting football analytics and visuals
- [StatsBomb](https://statsbomb.com/) - great visual design and free open-data
- [John Burn-Murdoch](https://twitter.com/jburnmurdoch/status/1057907312030085120) - this tweet got me interested in soccer analytics.

## Contributions
Contributions are welcome. It would be great to add the following functionality:
- pass maps
- pass sonars
- voronoi diagrams

Examples to help others are also welcome for a gallery.

Please get in touch at rowlinsonandy@gmail.com or [@numberstorm](https://twitter.com/numberstorm) on Twitter.

## License
[MIT](https://choosealicense.com/licenses/mit/)