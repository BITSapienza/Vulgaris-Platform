<script>
export default {
	data: function() {
		return {
		}
	},
}
</script>

<template>
  <div>
    <div class="TitlePageHome">
      Contact Us
    </div>
  </div>
  <div class="bodyHome">
    <div class="sectionHome">
      Who are we
    </div>
    <div class="contentHome">
      We are computer science students from <span class="span-underline span-red">La Sapienza University of Rome</span>. 
      <br />
      For any issue & feedback please contact us via github &#128077;
      <div class="contact-git">
        <a href="https://github.com/federico-rosatelli/" target="_blank" title="Federico Rosatelli">
          <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="">
          <div class="username-git">
            federico-rosatelli
          </div>
        </a>
        <a href="https://github.com/AxnNxs/" target="_blank">
          <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="">
          <div class="username-git">
            AxnNxs
          </div>
        </a>
        <a href="https://github.com/Samseys" target="_blank">
          <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="">
          <div class="username-git">
            Samseys
          </div>
        </a>
        <a href="https://github.com/Loriv3" target="_blank">
          <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="">
          <div class="username-git">
            Loriv3
          </div>
        </a>
        <a href="https://github.com/BboyCaligola" target="_blank">
          <img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="">
          <div class="username-git">
            BboyCaligola
          </div>
        </a>
      </div>
    </div>
    
  </div>
</template>

<style>

.contact-git{
  margin-top: 50px;
  padding-bottom: 50px;
  display: flex;
  gap: 1%;
  width: 100%;
  text-align: center;
}
.contact-git img{
  border-radius: 50%;
  width: 80%;
}

.username-git{
  margin-top: 10px;
}

.span-red{
  color: #822433;
}
.contact-form{
    margin-left: 20%;
    margin-right: 20%;
    border: 1px solid #111;
    border-radius: 20px;
    transition: 0.4s;
}

.contact-form:hover{
    box-shadow: 10px 10px 10px rgba(24, 24, 24, 0.3);
}

input:focus ~ label, textarea:focus ~ label, input:valid ~ label, textarea:valid ~ label {
    font-size: 0.75em;
    color: #999;
    top: -5px;
    -webkit-transition: all 0.225s ease;
    transition: all 0.225s ease;
}

.styled-input {
    float: left;
    width: 293px;
    margin: 1rem 0;
    position: relative;
    border-radius: 4px;
}

@media only screen and (max-width: 768px){
    .styled-input {
        width:100%;
    }
}

.styled-input label {
    color: #999;
    padding: 1.3rem 30px 1rem 30px;
    position: absolute;
    top: 10px;
    left: 0;
    -webkit-transition: all 0.25s ease;
    transition: all 0.25s ease;
    pointer-events: none;
}

.styled-input.wide { 
    width: 650px;
    max-width: 100%;
}

input,
textarea {
    padding: 30px;
    border: 0;
    width: 100%;
    font-size: 1rem;
    background-color: #111;
    color: white;
    border-radius: 4px;
}

input:focus,
textarea:focus { outline: 0; }

input:focus ~ span,
textarea:focus ~ span {
    width: 100%;
    -webkit-transition: all 0.075s ease;
    transition: all 0.075s ease;
}

textarea {
    width: 100%;
    min-height: 15em;
}

.input-container {
    width: 650px;
    max-width: 100%;
    margin: 20px auto 25px auto;
}

.submit-btn {
    /* float:right; */
    padding: 2% 5%;
    border-radius: 10px;
    display: inline-block;
    background-color: #d6a315dc;
    color: white;
    font-size: 18px;
    cursor: pointer;
    box-shadow: 0 2px 5px 0 rgba(0,0,0,0.06),
              0 2px 10px 0 rgba(0,0,0,0.07);
    -webkit-transition: all 300ms ease;
    transition: all 300ms ease;
}

.submit-btn:hover {
    transform: translateY(3px);
    box-shadow: 0 1px 1px 0 rgba(0,0,0,0.10),
              0 1px 1px 0 rgba(0,0,0,0.09);
}


@media (max-width: 768px) {
    .submit-btn {
        width:100%;
        float: none;
        text-align:center;
    }
}

input[type=checkbox] + label {
  color: #ccc;
  font-style: italic;
} 

input[type=checkbox]:checked + label {
  color: #d6a315dc;
  font-style: normal;
}

.id-btn{
    padding: 7px 35px;
    border-radius: 60px;
    display: inline-block;
    margin-left: 40%;
    margin-right: 40%;
    margin-bottom: 5%;
    font-size: 18px;
    box-shadow: 0 2px 5px 0 rgba(0,0,0,0.06),
              0 2px 10px 0 rgba(0,0,0,0.07);
}
</style>