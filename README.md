# telegramBOT--ACCOUNTANT
import telebot

MypyBot = telebot.TeleBot('TOKEN', parse_mode = None)

@MypyBot.message_handler(content_types = ['text'])
def replyer(message):
    MypyBot.reply_to(message, message.text)

MypyBot.polling()
import telebot 
import config 
bot = telebot.TeleBot(config.TOKEN)
@bot.message_handler(content_types = ['text'])
def lalala(message):
    bot.send_message (message.chat.id, message.text)
bot.polling(none_stop = True)
