desc "Create a new blog post"
task :post do
  print "Please enter in the title of the blog post: "
  title = $stdin.gets.chomp.strip
  name = title.gsub(/\s+/, '-')
  name = name.gsub(/[^a-zA-Z0-9_-]/, "").downcase
  time = Time.now.strftime("%Y-%m-%d")
  File.open("_posts/#{time}-#{name}.textile", "w+") do |file|
    file.puts <<-EOF
--- 
title: #{title}
layout: post
---
    EOF
  end
  puts "Created '_posts/#{time}-#{name}.textile'"
end
