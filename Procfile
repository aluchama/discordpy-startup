discordbot: python discordbot.py
import discord
import random

Intents = discord.Intents.default()
Intents.members = True

TOKEN = 'OTY3Mzc0NzA4ODIxNTk4MjU4.YmPX5w.J_0YqarrtWTPhmp5xCGpZ7xQmwc' # TOKEN
CHANNELID = 906051578170052658 # チャンネルID

client = discord.Client(intents=Intents)

@client.event
async def on_ready():
    print('ログイン完了！')

@client.event
async def on_message(message):
    if not message.author.bot:
        channel = client.get_channel(CHANNELID)
        topic = '!BBP' #反応する文字列
        role = message.guild.get_role(967446652350787645)
        role_member = role.members
        member = random.choice(role_member)
        text1 = ':tada: :tada: :tada: **' + str(member) +'**:confetti_ball::confetti_ball::confetti_ball:'
        embed = discord.Embed( # Embedを定義する
                          title="当選者は…！",# タイトル
                          color=1502975, # フレーム色指定
                          description= text1 # 文章の中身
                          )
        embed.set_image(url="https://cdn.eriones.com/img/icon/ls_nq/a288dc75b51.png")
        if message.content == topic:
            await channel.send(embed = embed)
            print(text1)
            
client.run(TOKEN)
