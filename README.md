[![NPM](https://nodei.co/npm/react-grid-carousel.png?compact=true)](https://nodei.co/npm/react-grid-carousel/)  
[![GitHub license](https://img.shields.io/github/license/x3388638/react-grid-carousel)](https://github.com/x3388638/react-grid-carousel/blob/master/LICENSE) [![npm version](https://badge.fury.io/js/react-grid-carousel.svg)](https://badge.fury.io/js/react-grid-carousel) [![Open Source](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://opensource.org/)

<h1 align="center">React Grid Carousel</h1>
<p align="center">Flexible carousel layout w/ css grid<br />to easily create a carousel like photo gallery, shopping product card or anything you want</p>

<p align="center">
<img src="https://gist.githubusercontent.com/x3388638/82e341b43990c7851c9438dfdec43e3b/raw/69d266ba9f7140994eefb5bb9623d7bd339a12ae/demo2.gif" width="400px" />
<img src="https://gist.githubusercontent.com/x3388638/82e341b43990c7851c9438dfdec43e3b/raw/69d266ba9f7140994eefb5bb9623d7bd339a12ae/demo1.gif" width="100%" />
<img src="https://gist.githubusercontent.com/x3388638/82e341b43990c7851c9438dfdec43e3b/raw/69d266ba9f7140994eefb5bb9623d7bd339a12ae/demo3.gif" width="600px" />
</p>

## Features

- RWD
- Multiple items
- Multiple rows
- Infinite loop
- Support any component as a item to put into grid
- Show/hide dots
- Show/hide arrow buttons
- Auto play
- Enable/Disable `scroll-snap` for each item on mobile device
- Customized layout (cols & rows) for different breakpoint

## Install

```bash
$ npm install react-grid-carousel --save
```

## Usage

Just import the `Carousel` component from `react-grid-carousel`  
and put your item into `Carousel.Item`

```javascript
import React from 'react'
import Carousel from 'react-grid-carousel'

const Gallery = () => {
  return (
    <Carousel cols={2} rows={1} gap={10} loop>
      <Carousel.Item>
        <img width="100%" src="https://picsum.photos/800/600?random=1" />
      </Carousel.Item>
      <Carousel.Item>
        <img width="100%" src="https://picsum.photos/800/600?random=2" />
      </Carousel.Item>
      <Carousel.Item>
        <img width="100%" src="https://picsum.photos/800/600?random=3" />
      </Carousel.Item>
      <Carousel.Item>
        {/* anything you want to show in the grid */}
      </Carousel.Item>
      {/* ... */}
    </Carousel>
  )
}
```

## Props

| Prop                                  | Type    | Default   | Description                                               |
| ------------------------------------- | ------- | --------- | --------------------------------------------------------- |
| cols                                  | Number  | 1         | Column amount rendered per page                           |
| rows                                  | Number  | 1         | Row amount rendered per page                              |
| gap                                   | Number  | 10        | Margin (grid-gap) between each item/grid (px)             |
| loop                                  | Boolean | false     | Infinite loop or not                                      |
| scrollSnap                            | Boolean | true      | `true` for applying `scroll-snap` to items on mobile      |
| hideArrow                             | Boolean | false     | Show/hide the arrow prev/next buttons                     |
| showDots                              | Boolean | false     | Show dots indicate the current page on desktop mode       |
| autoplay                              | Number  |           | Autoplay timeout in ms; `undefined` for autoplay disabled |
| dotColorActive                        | String  | '#795548' | Valid css color value for active dot                      |
| dotColorInactive                      | String  | '#ccc'    | Valid css color value for inactive dot                    |
| [responsiveLayout](#responsiveLayout) | Array   |           | Customized cols & rows on different viewport size         |
| mobileBreakpoint                      | Number  | 767       | The breakpoint(px) to switch to default mobile layout     |
| containerClassName                    | String  |           | Classname for carousel container                          |
| containerStyle                        | Object  |           | Style object for carousel container                       |

### responsiveLayout

Array of layout settings for each breakbpoint

#### Setting options

`breakpoint`: Number; Requried; Equals to `max-width` used in media query, in px unit  
`cols`: Number; Column amount in this breakpoint layout  
`rows`: Number; Row amount in this breakpoint layout  
`gap`: Number; Gap size in this breakpoint layout

e.g.

```
[
  {
    breakpoint: 800,
    cols: 3,
    rows: 1,
    gap: 10
  }
]
```

## Example

Storybook (Don't forget to try on different viewport size)

```bash
$ git clone https://github.com/x3388638/react-grid-carousel
$ cd react-grid-carousel
$ npm ci
$ npm run storybook
```

Use case in real world

```bash
# clone & install packages
$ npm run dev
# open localhost:8080
```

or visit https://react-grid-carousel.now.sh/#use-case-in-real-world

## TODOs

- [ ] customized arrow button
- [ ] customized dot

## LICENSE

MIT
