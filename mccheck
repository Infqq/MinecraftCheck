from mcstatus import MinecraftServer
from vkbottle import Bot, Message

bot=Bot('токен группы')


@bot.on.message_handler(text='чек <check>', lower = True)
async def minecraft(ans: Message, check):
  try:
      server = MinecraftServer.lookup(check)
      status = server.status()
      await ans("Онлайн сервера: {0} \n Пинг: {1} ms".format(status.players.online, status.latency))
  except:
    await ans('Ошибка')
 

bot.run_polling()
