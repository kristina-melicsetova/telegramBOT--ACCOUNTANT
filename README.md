# telegramBOT--ACCOUNTANT
import telebot

MypyBot = telebot.TeleBot('TOKEN', parse_mode = None)

@MypyBot.message_handler(content_types = ['text'])
def replyer(message):
    MypyBot.reply_to(message, message.text)

MypyBot.polling()
