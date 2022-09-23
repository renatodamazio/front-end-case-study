# Feature
## New Components:

- **Avatar**
- **Chips**
- **Card**
- **TheTags**
- **TheUserCarousel**

## New Fonts:
- **TeX Gyre Adventor'**

## Bugfix:
- **Behavioral bug**: The sidebar should automatically close when a click event outside of it occurs
- **Behavioral bug**: The sidebar should automatically close after a page transition
- **UI bug**: The sidebar should be fixed and should not be affected by scrolling behavior
- **Refactor**: The sidebar should be refactor to use the Composition API

## Refactor:
- TheLanding Vue3 Composition

## Snapshot new Component (Card, Carousel, Avatar, Chip)
![Untitled](https://user-images.githubusercontent.com/39681291/191949235-99edebc2-5bfc-4b62-91d2-33b1c29035aa.png)

### TheUserCarousel
Using Vue3 carousel (https://ismail9k.github.io/vue3-carousel/). Renders the Card component:
- Props: expect [user, usersImageURL, tags, likes, views, previewURL]
- https://pixabay.com/api/?key=30053638-dc58052ebc04d497829e1a757&q=city&image_type=photo (loading in TheLanding.vue)

### Card:
Render composition components and shows user's information
- Props: expect [user, usersImageURL, tags, likes, views, previewURL]
- convertNumber(): converts and summarizes numbers according to quantity, ie: 1000 = 1k

### Avatar.vue
To render user image.
- Prop: src (image url or path)
- In case of image loading errors, the "flag" image will be loaded.
![Untitled2](https://user-images.githubusercontent.com/39681291/191951459-7cfccdfa-5a9e-4630-b7c0-981508270b40.png)


### TheTags.vue
- Iterates through the array of tags and renders the Chips component

### Chips.
- Accept a slot with text or HTML element.

### TheCarousel. 
- Render Vue3 carousel.
- Render Card component.

New web-fonts folder, with converted web-optimized fonts.
