# Devise gem으로 회원가입 구현하기
+ gem 'devise'추가
+ rails g devise:install
+ rails g devise User
+ rake db:migrate

## index파일
```ruby
<% if user_signed_in? %>
  <%= link_to 'sign out', destroy_user_session_path,method: 'delete'%>
<% else %>
  <%= link_to 'sign in',new_user_session_path %>
  <%= link_to 'sign up',new_user_registration_path %>
<%end %>
```

## 회원가입 관련 view 수정
+ 1.rails g devise:views 명령어로 하거나
+ 2.gem devise-19n 사용

## gem 'devise-i18n'
+국제화 도와주는 젬
+ config에 application.rb 에서 config.i18n.default_locale = :ko로 해줌