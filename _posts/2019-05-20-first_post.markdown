---
layout: post
title:  "jekyll github 연동하기"
date:   2019-05-20 00:22:33 +0900
categories: jekyll update
---
ruby 설치
brew cask install ruby
 brew install ruby-build
rbenv rehash

zshrc에 path 추가 및 eval "$(rbenv init -)"
source ./zshrc

rbenv versions 확인
rbenv global (위에나온 버전이랑 같은버전으로 맞추기)
ruby —version 확인

gem env 에 
Ruby Version 과 RUBY EXECUTABLE path가 system 으로 시작하지않고 로컬로 시작해야 user 권한으로 gem 이용 가능.

gem install jekyll bundler

—————————
jekyll local 에서 띄우기 
원하는 폴더위치에서 jekyll new injokly
injokly 폴더 생성됨.
vi Gemfile 해서
먼저 gem "jekyll", "~> 3.7.0" 이라고 쓰인 부분을 커멘트 처리한다.
그 다음 커맨트 처리되어 있는 gem "github-pages", group: :jekyll_plugins 부분을 커맨트 처리 해제하고 저장한다.

bundle install
bundle update

bundle exec jekyll serve //로컬 실행
http://127.0.0.1:4000/   에 접속하면 로컬띄운거 확인 가능

————————————git 연동
github에서 repository 생성

아까 생성한 로컬 디렉토리에서 
git init

//github push
git remote add origin ‘깃험주소’
git add -A
git commit -m ‘커밋할때 쓰일 메시지’
git push origin master
-> id/pw 입력 injokly@gmail.com / ..

https://injokly.github.io 로 접속하면 확인 가능

_config.yml 에서 타이틀, 내용 이메일 등등 수정 가능

블로그의 글은 _posts 폴더에 작성하며 아래와 같이 반드시 YYYY-MM-DD-제목.md 의 형식으로 파일 이름을 지정해야함



Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
