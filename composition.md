### Composition is:

to combine simple functions to build more complicated ones

Benefits of Composition
Because the concept of composition is such a large part of what makes React awesome and incredible to work with, let's dig into it a little bit. Remember that composition is just combining simple functions together to create complex functions. There are a couple of key ingredients here that we don't want to lose track of. These ingredients are:

    simple functions
    combined to create another function
    
Composition is built from simple functions. Let's look at an example:

    function getProfileLink (username) {
      return 'https://github.com/' + username
    }
    
This function is ridiculously simple, isn't it? It's just one line! Similarly, the getProfilePic function is also just a single line:

    function getProfilePic (username) {
      return 'https://github.com/' + username + '.png?size=200'
    }
These are definitely simple functions, so to compose them, we'd just combine them together inside another function:

    function getProfileData (username) {
      return {
        pic: getProfilePic(username),
        link: getProfileLink(username)
      }
    }
Now we could have written getProfileData without composition by providing the data directly:

    function getProfileData (username) {
      return {
        pic: 'https://github.com/' + username + '.png?size=200',
        link: 'https://github.com/' + username
      }
    }
There's nothing technically wrong with this at all; this is entirely accurate JavaScript code. But this isn't composition. There are also a couple of potential issues with this version that isn't using composition. If the user's link to GitHub is needed somewhere else, then duplicate code would be needed. A good function should follow the "DOT" rule:

    Do One Thing
    
This function is doing a couple of different (however minor) things; it's creating two different URLs, storing them as properties on an object, and then returning that object. In the composed version, each function just does one thing:

    getProfileLink – just builds up a string of the user's GitHub profile link
    getProfilePic – just builds up a string the user's GitHub profile picture
    getProfileData – returns a new object
    
React & Composition
React makes use of the power of composition, heavily! React builds up pieces of a UI using components. Let's take a look at some pseudo code for an example. Here are three different components:

    <Page />
    <Article />
    <Sidebar />
Now let's take these simple components, combine them together, and create a more complex component (aka, composition in action!):

    <Page>
      <Article />
      <Sidebar />
    </Page>
    
Now the Page component has the Article and Sidebar components inside. This is just like the earlier example where getProfileData had getProfileLink and getProfilePic inside it.

We'll dig into components soon, but just know that composition plays a huge part in building React components.
Composition Recap
Composition occurs when simple functions are combined together to create more complex functions. Think of each function as a single building block that does one thing (DOT). When you combine these simple functions together to form a more complex function, this is composition.


