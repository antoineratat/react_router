# React Router

# Table of contents

1. [Project description](#description)
2. [Installation instructions](#installation)
3. [Project structure](#structure)
4. [Explainations](#explainations)
5. [Screenshots](#screenshots)

## 1. Project description<a name="description"></a>

This project is a simple implementation of React Router.

Components are the heart of React's powerful, declarative programming model. React Router is a collection of navigational components that compose declaratively with your application. Whether you want to have bookmarkable URLs for your web app or a composable way to navigate in React Native

## 2. Installation instructions<a name="installation"></a>

Versions:

-   Node: 14.15.1
-   Npm: 6.14.8
-   React: 17.0.1

Download code from Github:

```shell
git clone https://github.com/antoineratat/react_router.git
```

Navigate to project directory.

```shell
cd react_intersection_observer
```

Install node modules.

```shell
npm install
```

Run the app in development mode. Open http://localhost:3000 to view it in the browser.

```shell
npm start
```

## 3. Project structure<a name="structure"></a>

-   src
    -   App.js
    -   App.css
    -   components
        -   About.js
        -   Error_404.js
        -   Home.js
        -   Navigation.js
        -   Todo.js
        -   TodoContainer.js
        -   TodoList.js

## 4. Explainations<a name="explainations"></a>

Step 1 — Initially render grey image (loading image)

```shell
<img alt={author} src={grey} />
```

Step 2 - Set up Ref

```shell
import React, { useRef } from 'react'
const thisImage = useRef()
<img ref={thisImage} alt={author} src={grey} />
```

Step 3 — Set up detection

```shell
useEffect(() => {
		let observer = new IntersectionObserver(
			(entries) =>
				entries.forEach((entry) => {
					if (entry.isIntersecting) {
						console.log('intersect')
						thisImage.current.src = url
						observer = observer.disconnect()
					}
				}),
			{ rootMargin: '0px 0px 200px 0px' }
		)
		observer.observe(thisImage.current)
	}, [url])
```

## 5. Screenshots<a name="screenshots"></a>

![React Router Screenshot](https://github.com/antoineratat/react_lazyloading/blob/main/screenshots/1.PNG?raw=true)
