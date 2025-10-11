# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Wald test for a term in a regression model Use regTermTest (survey) With (In) R Software
install.packages("survey")
library("survey")
regTermTest = read.csv("https://raw.githubusercontent.com/timbulwidodostp/regTermTest/main/regTermTest/regTermTest.csv",sep = ";")
# Estimation Wald test for a term in a regression model Use regTermTest (survey) With (In) R Software
model1 <- glm(cbind(ncases, ncontrols) ~ agegp + tobgp * alcgp, data = regTermTest, family = binomial())
regTermTest_1 <- regTermTest(model1,"tobgp")
regTermTest_1
regTermTest_2 <- regTermTest(model1,"tobgp:alcgp")
regTermTest_2
regTermTest_3 <- regTermTest(model1, ~alcgp+tobgp:alcgp)
regTermTest_3
# Wald test for a term in a regression model Use regTermTest (survey) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished