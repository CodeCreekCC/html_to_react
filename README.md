# HTML to React
Convert annotated HTML exported from [Bootstrap Studio](https://bootstrapstudio.io/) to React components.

## Sample
```html

<!-- Start: About Us -->
<div id="about_us" class="highlight-clean">
    <div class="container">
        <!-- Start: Intro -->
        <div class="intro">
            <h2 class="text-center section_heading"><strong>ALL-ROUND SOFTWARE DEVELOPMENT COMPANY</strong></h2>
            <p class="text-center section_text">Our cross-functional personnel work to create customized digital services that improve your productivity and market value. We are your reliable provider of software development and consulting services. We help you propel your SMEs to harness the power of advances in technology by create amazing digital experiences while optimizing and automating your operations.</p>
        </div><!-- End: Intro -->
    </div>
</div><!-- End: About Us -->

```

The above HTML snippet converts to the following directory structure:

```unix
|-src
   |-components
        |-about_us
            |-index.jsx
            |-intro
                |-index.jsx
        
```

And the individual components created are as follows:

```javascript

/* src/components/about_us/index.jsx */

import Intro from "./intro";

const AboutUs = (props) => {

    return (
        <div is="about_us" className="highlight-clean">
            <div className="container">
                <Intro />
            </div>
        </div>
    );
}

export default AboutUs;

```

```javascript

/* src/components/about_us/intro/index.jsx */

const Intro = (props) => {

    return (
        <div className="intro">
            <h2 className="text-center section_heading">
                <strong>
                    ALL-ROUND SOFTWARE DEVELOPMENT COMPANY
                </strong>
            </h2>
            <p className="text-center section_text">
                Our cross-functional personnel work to create customized digital services that improve your productivity and market value. We are your reliable provider of software development and consulting services. We help you propel your SMEs to harness the power of advances in technology by create amazing digital experiences while    optimizing and automating your operations.
            </p>
        </div>
    );
}

export default Intro;

```
