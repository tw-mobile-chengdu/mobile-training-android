# Build UI For Home Timeline

# Story

### Context
This is our first story build the real page, in this page we should display a post list and every post can tap and navigate to detail page.

### Scope

* Post card content
* Post list
* Post card click navigation

### Out Of Scope

* Post video and images display
* Link in the post content
* Pull to refresh
* Scroll to load more
* Header and footer toolbar

### Acceptance Criteria

| Given | When | Then |
| :--- | :--- | :--- |
| I as a weibo user | I open the mini weibo app | I can see the post list page(home timeline) |
| I as a weibo user | I land on home page | every post will display: 1. poster avatar, 2. weibo poster name, 3. weibo created datetime, 4. poster source, 5. post content, 6. post images, 7. share\comments\like icons
| I as a weibo user | I click the post | I can goto weibo detail page |

<img src="./images/06-weibo-home-timeline.jpeg" width=300 />

# Read First

* [Create a List with RecyclerView](https://developer.android.com/guide/topics/ui/layout/recyclerview)
* [Create a Card-Based Layout](https://developer.android.com/guide/topics/ui/layout/cardview)
* [Drawable resources](https://developer.android.com/guide/topics/resources/drawable-resource)
* [Layout resource](https://developer.android.com/guide/topics/resources/layout-resource)

* Test

When we build the UI of page, most of time we don't use the TDD, so in this story we don't have test cover the UI. in the real project, we use the e2e screen shot test to cover the UI of application.

* Network

Because this story is focus on UI building, so we create the dummy network module in the activity, in the real project, the network module should use DI or ref from global module.