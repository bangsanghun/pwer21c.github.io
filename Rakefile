require "rubygems"
require 'rake'
require 'yaml'
require 'time'
require 'open-uri'
require 'RMagick'
require "digest/md5"

SOURCE = "."
CONFIG = {
  'layouts' => File.join(SOURCE, "_layouts"),
  'posts' => File.join(SOURCE, "_posts")
}

###
# Based on jekyll-bootstrap's Rakefile.
# Thanks, @plusjade
# https://github.com/plusjade/jekyll-bootstrap
###

# Path configuration helper
module JB
  class Path
    SOURCE = "."
    Paths = {
      :layouts => "_layouts",
      :themes => "_includes/themes",
      :theme_assets => "_assets/themes",
      :theme_packages => "_theme_packages",
      :posts => "_posts"
    }
    
    def self.base
      SOURCE
    end

    # build a path relative to configured path settings.
    def self.build(path, opts = {})
      opts[:root] ||= SOURCE
      path = "#{opts[:root]}/#{Paths[path.to_sym]}/#{opts[:node]}".split("/")
      path.compact!
      File.__send__ :join, path
    end
  
  end #Path
end #JB


# Usage: rake post title="A Title" [date="2012-02-09"]
desc "Begin a new post in #{CONFIG['posts']}"
task :post do
  abort("rake aborted: '#{CONFIG['posts']}' directory not found.") unless FileTest.
    directory?(CONFIG['posts'])
  title = ENV["title"] || "new-post"
  slug = title.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '')
  begin
    date = (ENV['date'] ? Time.parse(ENV['date']) : Time.now).strftime('%Y-%m-%d')
  rescue Exception => e
    puts "Error - date format must be YYYY-MM-DD, please check you typed it correctly!"
    exit -1
  end
  filename = File.join(CONFIG['posts'], "#{date}-#{slug}.md")
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?",
      ['y', 'n']) == 'n'
  end

  puts "Creating new post: #{filename}"
  open(filename, 'w') do |post|
    post.puts "---"
    post.puts "layout: post"
    post.puts "title: \"#{title.gsub(/-/,' ')}\""
    post.puts "category: posts"
    post.puts "---"
  end
end # task :post

desc "Launch preview environment"
task :preview do
  system "bundle exec jekyll serve --watch --drafts"
end # task :preview

# Usage: rake page name="about.html"
# You can also specify a sub-directory path.
# If you don't specify a file extention we create an index.html at the path specified
desc "Create a new page."
task :page do
  name = ENV["name"] || "new-page.md"
  filename = File.join(SOURCE, "#{name}")
  filename = File.join(filename, "index.html") if File.extname(filename) == ""
  title = File.basename(filename, File.extname(filename)).gsub(/[\W\_]/, " ").gsub(/\b\w/){$&.upcase}
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?", ['y', 'n']) == 'n'
  end
  
  mkdir_p File.dirname(filename)
  puts "Creating new page: #{filename}"
  open(filename, 'w') do |post|
    post.puts "---"
    post.puts "layout: page"
    post.puts "title: \"#{title}\""
    post.puts 'description: ""'
    post.puts "---"
    post.puts "{% include JB/setup %}"
  end
end # task :page

# Usage: rake post title="A Title" [date="2012-02-09"]
desc "Begin a new post thesis in #{CONFIG['posts']}"
task :thesis do
  abort("rake aborted: '#{CONFIG['posts']}' directory not found.") unless FileTest.
    directory?(CONFIG['posts'])
  title = ENV["title"] || "new-post"
  slug = title.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '')
  begin
    date = (ENV['date'] ? Time.parse(ENV['date']) : Time.now).strftime('%Y-%m-%d')
  rescue Exception => e
    puts "Error - date format must be YYYY-MM-DD, please check you typed it correctly!"
    exit -1
  end
  filename = File.join(CONFIG['posts'], "#{date}-#{slug}.md")
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?",
      ['y', 'n']) == 'n'
  end

  puts "Creating new post: #{filename}"
  open(filename, 'w') do |post|
    post.puts "---"
    post.puts "layout: post"
    post.puts "title: \"#{title.gsub(/-/,' ')}\""
    post.puts "category: posts"
    post.puts "group: thesis"
    post.puts "---"
  end
end # task :thesis

# Usage: rake post title="A Title" [date="2012-02-09"]
desc "Begin a new post dsi in #{CONFIG['posts']}"
task :dsi do
  abort("rake aborted: '#{CONFIG['posts']}' directory not found.") unless FileTest.
    directory?(CONFIG['posts'])
  title = ENV["title"] || "new-post"
  slug = title.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '')
  begin
    date = (ENV['date'] ? Time.parse(ENV['date']) : Time.now).strftime('%Y-%m-%d')
  rescue Exception => e
    puts "Error - date format must be YYYY-MM-DD, please check you typed it correctly!"
    exit -1
  end
  filename = File.join(CONFIG['posts'], "#{date}-#{slug}.md")
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?",
      ['y', 'n']) == 'n'
  end

  puts "Creating new post: #{filename}"
  open(filename, 'w') do |post|
    post.puts "---"
    post.puts "layout: post"
    post.puts "title: \"#{title.gsub(/-/,' ')}\""
    post.puts "category: posts"
    post.puts "group: dsi"
    post.puts "---"
  end
end # task :thesis




desc "Update icons based on your gravatar (define author email in _config.yml)!"
task :icons do
  puts "Getting author email from _config.yml..."
  config = YAML.load_file('_config.yml')
  author_email = config['author']['email']
  gravatar_id = Digest::MD5.hexdigest(author_email)
  base_url = "http://www.gravatar.com/avatar/#{gravatar_id}?s=150"

  origin = "origin.png"
  File.delete origin if File.exist? origin

  puts "Downloading base image file from gravatar..."
  open(origin, 'wb') do |file|
    file << open(base_url).read
  end

  name_pre = "apple-touch-icon-%dx%d-precomposed.png"

  FileList["*apple-touch-ico*.png"].each do |img|
    File.delete img
  end

  FileList["*favicon.ico"].each do |img|
    File.delete img
  end

  puts "Creating favicon.ico..."
  Magick::Image::read(origin).first.resize(32, 32).write("favicon.ico")

  [144, 114, 72, 57].each do |size|
    puts "Creating #{name_pre} icon..." % [size, size]
    Magick::Image::read(origin).first.resize(size, size).
      write(name_pre % [size, size])
  end
  puts "Cleaning up..."
  File.delete origin
end

desc "Install libs required by theme"
task :init do
  puts "Downloading and installing required javascript plugins"
  `npm install -g grunt-cli bower`
  `npm install`
  `bower install`
  puts "Downloading Bootstrap and Font Awesome"
  `grunt`
end

