---
title: "Building a real-time mobile app with Elixir (part 1)"
date: 2021-06-23
draft: false
description: "Let's build a real-time app with Elixir!"
tags:
  - elixir
  - phoenix
  - mobile
---

In this series of posts, we will explore how we can use [Phoenix](https://www.phoenixframework.org/) to build a
real-time mobile app. You may have [already seen](https://www.youtube.com/watch?v=MZvmYaFkNJI) how you can do such cool
things for the web using [Phoenix LiveView](https://github.com/phoenixframework/phoenix_live_view). Here we'll cover
the case where you want to use the same powerful building blocks to power a mobile app instead.

Before we get started though, let's get some requirements/terminology out of the way first. More specifically, **what is
a real-time app**? For our case, we'll define this as an app where low latency (e.g. under 200msec) is crucial to the UX
of the app. Think, for example, apps like sports betting, auctions, trivia games, stock tickers, polling/voting, etc.
Games could also definitely fit into this category. People have even gone even crazier with LiveView and build things
like [flight simulators](https://github.com/joshprice/groundstation).

But why Elixir?

Of all the possibilities, the app we'll be building will be a trivia app. This could be an app used at your [favorite
trivia night](https://www.geekswhodrink.com/venues/702584896/) or even end up being a [massive online game](<https://en.wikipedia.org/wiki/HQ_(video_game)#HQ_Trivia>).
