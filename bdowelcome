import discord
import asyncio
from discord import Game
from discord.ext.commands import Bot
import datetime
import os


client = discord.Client()

@client.event
async def on_ready():
    print('Logged in')
    print('Name : {}'.format(client.user.name))
    print('ID : {}'.format(client.user.id))
    print(discord.__version__)

@client.event
async def on_member_join(member):
	await client.send_message(discord.Object(id='445964363711381505'), '\n{} ยินดีต้อนรับสู่ Discord สายม้าจ้า เรามีบอทไว้สำหรับแจ้งเตือนเวลาแข่งม้าด้วยนะ ถ้าไม่มีใครแจ้งเวลาให้บอทไว้สามารถใช้ได้ทุกคนน้า \n**วิธีการใช้งานต่าง**\n-วิธีการใช้งานบอทดูได้ที่ <#445198810470154240> \n-วิธีรับการแจ้งเตือนต่างๆดูได้ที่ <#450634340066394122> \n-สามารถพูดคุยสอบถามข้อมูลได้ที่ <#430014886962003972> \n\n -----------------------------------'.format(member.mention))

@client.event
async def on_message(message):
	st = message.content.split()
	if len(st) == 3:
		server = st[0]
		t = st[1]
		time = st[2]
		if server.upper() == '!B' or server.upper() == 'B' or server.upper() == 'S' or server.upper() == '!S' or server.upper() == 'ิ' or server.upper() == 'บา' or server.upper() == 'ห' or server.upper() == 'เซ' or server.upper() == 'บ' or server.upper() == 'ซ':
			if t.upper() == 'T1' or t.upper() == 'T2' or t.upper() == 'T3' or t.upper() == 'T4' or t.upper() == 'T5' or t.upper() == 'T6' or t.upper() == 'T7' or t.upper() == 'T8' or t.upper() == '1' or t.upper() == '2' or t.upper() == '3' or t.upper() == '4' or t.upper() == '5' or t.upper() == '6' or t.upper() == '7' or t.upper() == '8':
				if int(time) < 61:
					msg = await client.send_message(discord.Object(id='455792184294113300'), datetime.datetime.now().strftime('%Y-%m-%d %H:%M:%S') +'->('+ str(message.author) +')->\" '+message.content+' \"')
					await asyncio.sleep(10)
					await client.delete_message(message)


client.run(os.getenv('TOKEN'))
