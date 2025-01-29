### REST Client API untuk Discord v10

#### Mendapatkan Informasi Pengguna
```http
GET https://discord.com/api/v10/users/@me
Authorization: Bot YOUR_BOT_TOKEN
```

#### Mengambil Pesan dalam Channel
```http
GET https://discord.com/api/v10/channels/{channelId}/messages?limit={limit}
Authorization: Bot YOUR_BOT_TOKEN
```

#### Mengirim Pesan ke Channel
```http
POST https://discord.com/api/v10/channels/{channelId}/messages
Authorization: Bot YOUR_BOT_TOKEN
Content-Type: application/json

{
  "content": "Halo, Discord!"
}
```

#### Menghapus Pesan di Channel
```http
DELETE https://discord.com/api/v10/channels/{channelId}/messages/{messageId}
Authorization: Bot YOUR_BOT_TOKEN
```

#### Bergabung dengan Guild via Invite
```http
POST https://discord.com/api/v10/invites/{inviteCode}
Authorization: Bot YOUR_BOT_TOKEN
```

#### Keluar dari Guild
```http
DELETE https://discord.com/api/v10/users/@me/guilds/{guildId}
Authorization: Bot YOUR_BOT_TOKEN
```

#### Mendapatkan Peran di Guild
```http
GET https://discord.com/api/v10/guilds/{guildId}/roles
Authorization: Bot YOUR_BOT_TOKEN
```

#### Menambahkan Peran ke Anggota
```http
PUT https://discord.com/api/v10/guilds/{guildId}/members/{memberId}/roles/{roleId}
Authorization: Bot YOUR_BOT_TOKEN
```

#### Menghapus Peran dari Anggota
```http
DELETE https://discord.com/api/v10/guilds/{guildId}/members/{memberId}/roles/{roleId}
Authorization: Bot YOUR_BOT_TOKEN
```

#### Membuat Peran Baru di Guild
```http
POST https://discord.com/api/v10/guilds/{guildId}/roles
Authorization: Bot YOUR_BOT_TOKEN
Content-Type: application/json

{
  "name": "New Role",
  "permissions": "0",
  "color": 0
}
```

#### Memperbarui Peran di Guild
```http
PATCH https://discord.com/api/v10/guilds/{guildId}/roles/{roleId}
Authorization: Bot YOUR_BOT_TOKEN
Content-Type: application/json

{
  "name": "Updated Role"
}
```

#### Menghapus Peran di Guild
```http
DELETE https://discord.com/api/v10/guilds/{guildId}/roles/{roleId}
Authorization: Bot YOUR_BOT_TOKEN
```

#### Membisukan Anggota dalam Voice Channel
```http
PATCH https://discord.com/api/v10/guilds/{guildId}/members/{memberId}
Authorization: Bot YOUR_BOT_TOKEN
Content-Type: application/json

{
  "mute": true
}
```

#### Membuat Channel Baru di Guild
```http
POST https://discord.com/api/v10/guilds/{guildId}/channels
Authorization: Bot YOUR_BOT_TOKEN
Content-Type: application/json

{
  "name": "new-channel",
  "type": 0
}
```

#### Memperbarui Channel
```http
PATCH https://discord.com/api/v10/channels/{channelId}
Authorization: Bot YOUR_BOT_TOKEN
Content-Type: application/json

{
  "name": "updated-channel"
}
```

#### Menghapus Channel
```http
DELETE https://discord.com/api/v10/channels/{channelId}
Authorization: Bot YOUR_BOT_TOKEN
```

#### Menambahkan Reaksi ke Pesan
```http
PUT https://discord.com/api/v10/channels/{channelId}/messages/{messageId}/reactions/{emoji}/@me
Authorization: Bot YOUR_BOT_TOKEN
```

#### Menghapus Reaksi dari Pesan
```http
DELETE https://discord.com/api/v10/channels/{channelId}/messages/{messageId}/reactions/{emoji}/@me
Authorization: Bot YOUR_BOT_TOKEN
```

