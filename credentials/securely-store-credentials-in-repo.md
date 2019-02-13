# Securely Store Credentials in Repo

1) Run `rails credentials:edit` to open in Emacs edtior
2) Store credentials

```
aws:
  access_key_id: 123
  secret_access_key: 345
```

3) Ctrl + C, then `s` then `y` to save.
4) Share master key to team. Should not be pushed to repo.

Common Gotcha: 
```
'rescue in _decrypt': ActiveSupport::MessageEncryptor::InvalidMessage (ActiveSupport::MessageEncryptor::InvalidMessage)
```

1) Delete `credentials.yml.enc` and `master.key`
2) Run `rails credentials:edit`


Sources: 
https://guides.rubyonrails.org/security.html
https://www.engineyard.com/blog/rails-encrypted-credentials-on-rails-5.2