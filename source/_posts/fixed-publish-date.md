---
title: Test-Theme-Config
date: 2024-02-01 14:34:02
updated: 2024-02-01 14:34:02
tags:
---
Since posts are redeployed each time and the posting date of the post changes, I fixed this as [others have suggested](https://sqiang.net/post/2792803495.html).


1. Modify the file "/scaffolds/post.md" to add `updated: {{ date }}`.   

        ---
        title: {{ title }}
        date: {{ date }}
        updated: {{ date }}
        tags:
        ---

2. Modify the theme's "__config.yml", like below:

        # Post meta display settings
        post_meta:
            item_text: true
            created_at: true      
            # update_at set to true  
            updated_at:
                enable: true
                another_day: true
            categories: true