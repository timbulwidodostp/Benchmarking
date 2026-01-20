# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Stochastic frontier estimation (SFA) Use Benchmarking With (In) Software
install.packages("Benchmarking")
library("Benchmarking")
# Estimates Stochastic frontier estimation (SFA) Use Benchmarking With (In) Software
Benchmarking = read.csv("https://raw.githubusercontent.com/timbulwidodostp/Benchmarking/main/Benchmarking/Benchmarking.csv", sep = ";")
x <- cbind(log(Benchmarking$capital), log(Benchmarking$labour))
y <- matrix(log(Benchmarking$output))
sfa_ <- sfa(x,y)
Stochastic_frontier_estimation <- sfa_
te <- te.sfa(sfa_)
teM <- teMode.sfa(sfa_)
teJ <- teJ.sfa(sfa_)
Stochastic_frontier_estimation <- cbind(eff(sfa_),te,Mode=eff(sfa_, type="Mode"),teM,teJ)[1:16,]
sigma2 <- sigma2.sfa(sfa_)
lambda <- lambda.sfa(sfa_)
summary(sfa_)
Stochastic_frontier_estimation
sigma2
lambda
# Stochastic frontier estimation (SFA) Use Benchmarking With (In) Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished