# sentiment analysis  #
source file at https://github.com/bentrevett/pytorch-sentiment-analysis/blob/master/2%20-%20Upgraded%20Sentiment%20Analysis.ipynb
Modifications made as below.

*team members*

1. Chiranthan CV
2. Girish Nautiyal
3.Arghya
4.Madalasa Venkataraman


### Change this code in such a way that: ###

1. it has 3 LSTM layers

2. it has used a for loop to do so in the forward function

3. the dropout value used is 0.2

4. trained on the text that is reversed (for example "my name is Rohan" becomes "Rohan is name my"

5. achieves 87% or more accuracy

6. once done, share the Github link as well (after training on Google Colab, move the file to GitHub).


Steps

1. Changed max vocab size to double current size by using  glove.6B.200d instead of glove.6B.100d 

2. In batch definition, batch size retained as 64, but changed sort_within_batch = False

3. LSTM - three loops needed

#changed this code to represent three  LSTM 

        self.rnns = nn.ModuleList([
        
                      nn.LSTM(embedding_dim, 
                      
                           hidden_dim,
                           
                           bidirectional=bidirectional),
                           

                      nn.LSTM(hidden_dim, 
                      
                           hidden_dim,
                           
                           bidirectional=bidirectional),
                           

                      nn.LSTM(hidden_dim, 
                      
                           hidden_dim,
                           
                           bidirectional=bidirectional)
                           
        ])
        
  4. used for loop in forward
  
  for i, rnn in enumerate(self.rnns):
  
          packed_embedded, (hidden, cell) = rnn(packed_embedded)
          
          self.dropout(packed_embedded.data)
  
  5. Used  reverse_text = torch.flip(text, [0])
   and made sure both original and reverse texts were used for training.
  
  

### Learning ###

Ran out of cuda memory due to too many dilations on vocab size

Avg loss

	Train Loss: 0.018 | Train Acc: 99.57%
	 Val. Loss: 0.583 |  Val. Acc: 87.50%
