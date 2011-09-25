<pre><code>
mkdir gitblog
cd gitblog/
mkdir master && cd master
git init
echo "# Master" > README.markdown
git add .
git commit -m "Master added"
git remote add origin git@github.com:vlpeng/gitblog.git
git push origin master
cd .. && mkdir gh-pages && cd gh-pages/
git clone git://github.com/coolaj86/jekyll-aid.git .
git remote rm origin
git remote add origin git@github.com:vlpeng/gitblog.git
git symbolic-ref HEAD refs/heads/gh-pages
rm .git/index
git add .
git commit -a -m "First pages commit"
git push origin :gh-pages && git push origin gh-pages
./mkdocument 'Title of my Awesome-blog post!!!'
git add .
git commit -am 'add 1st post'
git push origin gh-pages
</pre></code>
