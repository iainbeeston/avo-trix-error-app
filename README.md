# README

Sample rails app to reproduce a bug in avo 2.34.1.

To reproduce the issue:

1. start the app using `bin/rails s`
2. go to http://localhost:3000/avo

In avo, if you try to create a new person you should see this error:

    undefined method `html_safe' for #<ActionText::RichText id: nil, name: "biography", body: nil, record_type: "Person", record_id: nil, created_at: nil, updated_at: nil>

If you try to edit a person (you might have to create them via the rails console first) you should see the same error.
