---
title: "Android: Link Activity to ViewModel"
description: "How can I get the ViewModel for my Activity again?"
image: 
date: 2020-11-03T13:40:30+01:00
type: blog
---

In your Activity, how do you access your ViewModel again? This is a question I constantly ask myself, also because the default solution of Android Studio's templates is deprecated. 

Here's the solution:

```kotlin
class MyActivity : AppCompatActivity() {

  override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_my)

    val viewModel = ViewModelProvider(this).get(MyViewModel::class.java)
  }
}
```

Hope that helps anyone.  
At least I now know where to look it up quickly. 😁