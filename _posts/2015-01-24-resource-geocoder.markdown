---
layout: post
title: "resource :geocoder"
date: 2015-01-24 18:32:00 -0800
comments: true
categories: [Ruby on Rails, Resources, Routes]
---

Resourceful route **Memorize This**

`resource :photos`

creates seven different routes in your application, all mapping to the Photos controller:

|HTTP Verb       |Path                | Controller#Action      | Used for                                    |
|  ------------- |     ---------------|  ----------------------| ------------------------------------------- |
|`GET`           | `/photos`          | `photos#index`         | Display a list of all photos                |
|`GET`           | `/photos/new`      | `photos#new`           | Return an HTML form for creating a new photo|
|`POST`          | `/photos`          | `photos#create`        | Create a new photo                          |
|`GET`           | `/photos/:id`      | `photos#show`          | Display a specific photo                    |
|`GET`           | `/photos/:id/edit` | `photos#edit`          | Return an HTML form for editing a photo     |
|`PATCH/PUT`     | `/photos/:id`      | `photos#update`        | Update a specific photo                     |
|`DELETE`        | `/photos/:id`      | `photos#destroy`       | Delete a specific photo                     |

From [RailsGuides](http://guides.rubyonrails.org/routing.html#defining-multiple-resources-at-the-same-time)

