# wad21exam1

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

# Setup:

You need to [import](https://docs.github.com/en/github/importing-your-projects-to-github/importing-source-code-to-github/importing-a-repository-with-github-importer)   this [repository](https://github.com/M-Gharib/WAD21EXAM1)  to your GitHub account

**Note:** you have to be logged in to your GitHub account to do the following steps

- In the first field "Your old repository’s clone URL" enter URL of this repository https://github.com/M-Gharib/WAD21EXAM1
- In the "Your new repository details", give the repo a name, and make it **Private**
- Press on "begin import", it should take a few seconds
- Add me as a collaborator to your new repository (inviting collaborators)
- My email and username on GitHub are: mohamad.gharib@ut.ee and M-Gharib respectively


# Tasks:

 In router/index.js:

1. Add a route to the **Destinations.vue** view;

2. Do the required modification to remove any lazy loading route(s), i.e., no view in **router/index.js** should be lazy-loaded.

In App.vue,

3. Add rout link to the ** Destinations.vue**  view. This link should appear between the **Home**  and **About**  links.

4. Modify the **destination_comp.vue** to display all destinations objects in the destinationList array, which exist in the **Destinations.vue** view, i.e., destinationList should be passed to **destination_comp.vue** from the **Destinations.vue** view.

5. Move the destinationList array from **Destinations.vue** to the **state {}** within **index.js** file in the store (**store/index.js**). Then, do the required modifications so that the **Destinations.vue** works in the same way as it used to work before these modifications, i.e., there should be no difference in the appearance of the **Destinations.vue** after moving the destinationList array to the store.

6. Create a **getter** in the **getters {}** within **index.js** file in the **store (store/ index.js)**. Call it **destinationListDiscount**, which should contain the same information as the destinationList array except for the **price**, which needs to be reduced by **50% (e.g., price/2)**.

7. Do the required modifications so that **destination_comp.vue** will represent the information contained within **destinationListDiscount** instead of **destinationList**.

8. Within the **destination_comp.vue**, create a button (**call it "Apply coupon"**), which when pressed shall reduce the price of **all the tickets by 1 euro**.

**Note:** destination_comp.vue is representing information coming from a getter (destinationListDiscount), not from the state {} (destinationList). It is better to try to apply the required modification (-1 euro) to the destinationList instead of destinationListDiscount.
