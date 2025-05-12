# ee2703-week-9--spectra-of-non-periodic-signals-solved
**TO GET THIS SOLUTION VISIT:** [EE2703 Week 9- Spectra of non-periodic signals Solved](https://www.ankitcodinghub.com/product/ee2703-week-9-spectra-of-non-periodic-signals-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;90796&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE2703 Week 9-&nbsp;Spectra of non-periodic signals Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;Spectra of non-periodic signals

In the previous assignment we looked at functions that were periodic and extracted their spectra. The approach was:

<ul>
<li>Sample the signal so that fNyquist is met, and so that ∆f is small enough. Generate the frequency axis from − fmax/2 to + fmax/2, taking care to drop the last term.</li>
<li>Ensurethatthesignalstartsatt=0+ andendsatt=0−</li>
<li>Use 2k samples</li>
<li>Obtain the DFT. Rotate the samples so that they go from f = − fmax/2 to f = +fmax/2−∆f.</li>
<li>Plot the magnitude and phase of the spectrum. Usually we would plot the magnitude in dB and the phase in degrees and the frequency axis would be logarithmic. This is to capture polynomial decay of the spectrum.</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
Nowwewanttolookatnon-periodicsignals.Ourfirstsignalwillbesin over 0 to 2π with 64 samples, this function looks as follows:

1 ⟨* 1⟩≡ ⟨eg1 2⟩

</div>
<div class="column">
􏰆√ 􏰇

2t .Obtained

</div>
</div>
<div class="layoutArea">
<div class="column">
26 March 2019

April 18, 2018

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
2 ⟨eg1 2⟩≡ (1) from pylab import *

<pre>      t=linspace(-pi,pi,65);t=t[:-1]
      dt=t[1]-t[0];fmax=1/dt
      y=sin(sqrt(2)*t)
      y[0]=0 # the sample corresponding to -tmax should be set zeroo
      y=fftshift(y) # make y start with y(t=0)
      Y=fftshift(fft(y))/64.0
      w=linspace(-pi*fmax,pi*fmax,65);w=w[:-1]
</pre>
<pre>      figure()
      subplot(2,1,1)
      plot(w,abs(Y),lw=2)
      xlim([-10,10])
      ylabel(r"$|Y|$",size=16)
      title(r"Spectrum of $\sin\left(\sqrt{2}t\right)$")
      grid(True)
      subplot(2,1,2)
      plot(w,angle(Y),’ro’,lw=2)
      xlim([-10,10])
      ylabel(r"Phase of $Y$",size=16)
      xlabel(r"$\omega$",size=16)
      grid(True)
      savefig("fig10-1.png")
      show()
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
We expected two spikes, but what we got were two peaks each with two values and a gradually decaying magnitude. The phase is correct though – but take a look at the code. There is one line there:

<pre>    y[0]=0 # the sample corresponding to -tmax should be set zero
</pre>
What is this for? An antisymmetric function has a purely imaginary fourier transform. But what about an antisymmetric set of samples? Suppose

</div>
</div>
<div class="layoutArea">
<div class="column">
y[0] = y[i] =

y[N2 ] =

The DFT of this sequence will give us

N−1 􏰃2πj 􏰄 Y[k] = ∑y[n]exp Nkn

n=0

</div>
<div class="column">
sin(0)

i = 1,2… N2 −1

sin(−tmax)

</div>
</div>
<div class="layoutArea">
<div class="column">
0

−y[N −i]

</div>
</div>
<div class="layoutArea">
<div class="column">
sin􏰁tN/2􏰂

</div>
</div>
<div class="layoutArea">
<div class="column">
N/2−1 􏰃 􏰃2πj 􏰄 􏰃 2πj 􏰄􏰄 N

= ∑ y[n] exp N kn −exp − N kn +y[2]exp(πkj)

n=1

N/2−1 􏰃2π 􏰄 k N

= ∑−2jy[n]sin Nkn +(−1)y[2] n=1

But this is no longer pure imaginary! Since we need that property, we set y[N/2] to zero. That gives us a purely imaginary phase. But what to do about the magnitude? And what went wrong?

</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
To understand what went wrong, let us plot the time function over several time periods.

4 ⟨eg2 4⟩≡

from pylab import *

<pre>      t1=linspace(-pi,pi,65);t1=t1[:-1]
      t2=linspace(-3*pi,-pi,65);t2=t2[:-1]
      t3=linspace(pi,3*pi,65);t3=t3[:-1]
      # y=sin(sqrt(2)*t)
</pre>
<pre>      figure(2)
      plot(t1,sin(sqrt(2)*t1),’b’,lw=2)
      plot(t2,sin(sqrt(2)*t2),’r’,lw=2)
      plot(t3,sin(sqrt(2)*t3),’r’,lw=2)
      ylabel(r"$y$",size=16)
      xlabel(r"$t$",size=16)
      title(r"$\sin\left(\sqrt{2}t\right)$")
      grid(True)
      savefig("fig10-2.png")
      show()
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
The blue line connects the points whose DFT we took. The red lines show the con-

</div>
</div>
<div class="layoutArea">
<div class="column">
􏰆√ 􏰇

tinuation of the function. Quite clearly, even though sin 2t is a periodic function, the

</div>
</div>
<div class="layoutArea">
<div class="column">
portion between −π and π is not the part that can be replicated to generate the function. So which function is the DFT trying to fourier analyse? For that we have to replicate just the blue points. And that is shown below:

5 ⟨eg3 5⟩≡

from pylab import *

<pre>      t1=linspace(-pi,pi,65);t1=t1[:-1]
      t2=linspace(-3*pi,-pi,65);t2=t2[:-1]
      t3=linspace(pi,3*pi,65);t3=t3[:-1]
      y=sin(sqrt(2)*t1)
</pre>
<pre>      figure(3)
      plot(t1,y,’bo’,lw=2)
      plot(t2,y,’ro’,lw=2)
      plot(t3,y,’ro’,lw=2)
      ylabel(r"$y$",size=16)
      xlabel(r"$t$",size=16)
      title(r"$\sin\left(\sqrt{2}t\right)$ with $t$ wrapping every $2\pi$ ")
      grid(True)
      savefig("fig10-3.png")
      show()
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
􏰆√ 􏰇

Clearly this function is not sin 2t and that is why the DFT is not what we expect.

But why did that create the problem we saw above?

Gibbs Phenomenon

This is something you know very well. The Fourier transform of the box function

</div>
</div>
<div class="layoutArea">
<div class="column">
is given by

</div>
</div>
<div class="layoutArea">
<div class="column">
ramp:

Then the fourier series of this ramp is

</div>
</div>
<div class="layoutArea">
<div class="column">
􏰈1 |t|≤t0 0 |t|&gt;t0

F(ω) = 2sin(ωt0) ω

</div>
</div>
<div class="layoutArea">
<div class="column">
f(t)=

</div>
</div>
<div class="layoutArea">
<div class="column">
The spectrum of the box function decays very slowly, as 2/ω.

Now our function is an odd function with a big jump. So let us consider the periodic

</div>
</div>
<div class="layoutArea">
<div class="column">
f (t) = t, −π &lt; t &lt; π

􏰃sint sin2t sin3t 􏰄

</div>
</div>
<div class="layoutArea">
<div class="column">
f(t)=2 1 − 2 + 3 −…

</div>
</div>
<div class="layoutArea">
<div class="column">
Again the coefficients decay very slowly.

The DFT is just like the fourier series, except that both time and frequency are samples.

So, if the time samples are like a ramp, the frequency samples will decay as 1/ω. Let us

</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
verify this for the ramp itself

7 ⟨eg4 7⟩≡

from pylab import *

<pre>      t=linspace(-pi,pi,65);t=t[:-1]
      dt=t[1]-t[0];fmax=1/dt
      y=t
      y[0]=0 # the sample corresponding to -tmax should be set zeroo
      y=fftshift(y) # make y start with y(t=0)
      Y=fftshift(fft(y))/64.0
      w=linspace(-pi*fmax,pi*fmax,65);w=w[:-1]
</pre>
<pre>      figure()
      semilogx(abs(w),20*log10(abs(Y)),lw=2)
      xlim([1,10])
      ylim([-20,0])
      xticks([1,2,5,10],["1","2","5","10"],size=16)
      ylabel(r"$|Y|$ (dB)",size=16)
      title(r"Spectrum of a digital ramp")
      xlabel(r"$\omega$",size=16)
      grid(True)
      savefig("fig10-4.png")
      show()
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
7

</div>
</div>
</div>
<div class="page" title="Page 8">
<div class="layoutArea">
<div class="column">
Clearly the spectrum decays as 20 dB per decade, which corresponds to 1􏰅ω. The big jumps at nπ force this slowly decaying spectrum, which is why we don’t see the expected

</div>
</div>
<div class="layoutArea">
<div class="column">
􏰆√ 􏰇 spikesforthespectrumofsin 2t .

</div>
</div>
<div class="layoutArea">
<div class="column">
Windowing

So what do we do? Well the spikes happen at the end of the periodic interval. So we damp the function near there, i.e., we multiply our function sequence f [n] by a “window” sequence w[n]:

g(n) = f (n)w(n)

The new spectrum is got by convolving the two fourier transforms:

N−1

Gk = ∑ FnWk−n

n=0

Suppose fn is a sinusoid. Then Fk has two spikes. But the two spikes are now smeared out by Wk. So we expect to get broader peaks. But what this also does is to suppress the jump at the edge of the window. The window we will use is called the Hamming window:

􏰈0.54+0.46cos􏰁 2πn 􏰂 |n| ≤ N−1 w[n]= N−1 2

0 else

􏰆√ 􏰇

Let us look at our time sequence for sin 2t now . . .

8 ⟨eg5 8⟩≡

from pylab import *

<pre>      t1=linspace(-pi,pi,65);t1=t1[:-1]
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
8

</div>
</div>
</div>
<div class="page" title="Page 9">
<div class="layoutArea">
<div class="column">
<pre>t2=linspace(-3*pi,-pi,65);t2=t2[:-1]
t3=linspace(pi,3*pi,65);t3=t3[:-1]
n=arange(64)
wnd=fftshift(0.54+0.46*cos(2*pi*n/63))
y=sin(sqrt(2)*t1)*wnd
</pre>
<pre>figure(3)
plot(t1,y,’bo’,lw=2)
plot(t2,y,’ro’,lw=2)
plot(t3,y,’ro’,lw=2)
ylabel(r"$y$",size=16)
xlabel(r"$t$",size=16)
title(r"$\sin\left(\sqrt{2}t\right)\times w(t)$ with $t$ wrapping every $2\pi$ ")
grid(True)
savefig("fig10-5.png")
show()
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
9

</div>
</div>
</div>
<div class="page" title="Page 10">
<div class="layoutArea">
<div class="column">
The jump is still there, but it is much reduced. There is a little bit of magic in keeping some of the jump – it gives us an extra 10 db of suppression.

Now let us take the DFT of this sequence and see what we get:

10 ⟨eg6 10⟩≡

from pylab import *

<pre>       t=linspace(-pi,pi,65);t=t[:-1]
       dt=t[1]-t[0];fmax=1/dt
       n=arange(64)
       wnd=fftshift(0.54+0.46*cos(2*pi*n/63))
       y=sin(sqrt(2)*t)*wnd
</pre>
<pre>       y[0]=0 # the sample corresponding to -tmax should be set zeroo
       y=fftshift(y) # make y start with y(t=0)
       Y=fftshift(fft(y))/64.0
       w=linspace(-pi*fmax,pi*fmax,65);w=w[:-1]
</pre>
<pre>       figure()
       subplot(2,1,1)
       plot(w,abs(Y),lw=2)
       xlim([-8,8])
       ylabel(r"$|Y|$",size=16)
       title(r"Spectrum of $\sin\left(\sqrt{2}t\right)\times w(t)$")
       grid(True)
       subplot(2,1,2)
       plot(w,angle(Y),’ro’,lw=2)
       xlim([-8,8])
       ylabel(r"Phase of $Y$",size=16)
       xlabel(r"$\omega$",size=16)
       grid(True)
       savefig("fig10-6.png")
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
10

</div>
</div>
</div>
<div class="page" title="Page 11">
<div class="layoutArea">
<div class="column">
show()

</div>
</div>
<div class="layoutArea">
<div class="column">
11

</div>
</div>
</div>
<div class="page" title="Page 12">
<div class="layoutArea">
<div class="column">
Compare to our first plot and you can see that the magnitude is greatly improved. We

still have a peak that is two samples wide. But that is because 2 lies between 1 and 2, which are the two fourier components available. If we use four times the number of points we should get better results.

12 ⟨eg7 12⟩≡

from pylab import *

<pre>       t=linspace(-4*pi,4*pi,257);t=t[:-1]
       dt=t[1]-t[0];fmax=1/dt
       n=arange(256)
       wnd=fftshift(0.54+0.46*cos(2*pi*n/256))
       y=sin(sqrt(2)*t)
</pre>
<pre>       # y=sin(1.25*t)
       y=y*wnd
       y[0]=0 # the sample corresponding to -tmax should be set zeroo
       y=fftshift(y) # make y start with y(t=0)
       Y=fftshift(fft(y))/256.0
       w=linspace(-pi*fmax,pi*fmax,257);w=w[:-1]
       figure()
       subplot(2,1,1)
       plot(w,abs(Y),’b’,w,abs(Y),’bo’,lw=2)
       xlim([-4,4])
       ylabel(r"$|Y|$",size=16)
       title(r"Spectrum of $\sin\left(\sqrt{2}t\right)\times w(t)$")
       grid(True)
       subplot(2,1,2)
       plot(w,angle(Y),’ro’,lw=2)
       xlim([-4,4])
       ylabel(r"Phase of $Y$",size=16)
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
12

</div>
</div>
<div class="layoutArea">
<div class="column">
√

</div>
</div>
</div>
<div class="page" title="Page 13">
<div class="layoutArea">
<div class="column">
<pre>xlabel(r"$\omega$",size=16)
grid(True)
savefig("fig10-7.png")
show()
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
13

</div>
</div>
</div>
<div class="page" title="Page 14">
<div class="layoutArea">
<div class="column">
Is it better? Well it is quite a bit better since we are now zoomed in and see a lot more

detail. But why is it not just a single peak? The reason for that is w(t). Multiplication in

time is convolution in frequency and vice versa. So by multiplying with w(t), we got rid

of the 1/ f decay. But the delta function is now replaced by the shape of the DFT of w[n].

That gives us a factor of two broadening over the peak when there is no window, which is

why we still see a peak whose width is two samples.

</div>
</div>
<div class="layoutArea">
<div class="column">
√

</div>
</div>
<div class="layoutArea">
<div class="column">
Note that it is not because 2 is between 1.25 and 1.5. To verify, there is an alternate function in the above code, namely sin(1.25t). But this gives a broad peak as well. That is because of w[n].

The Assignment

<ol>
<li>Work through the example codes and understand them.</li>
<li>Considerthefunctioncos3(ω0t).Obtainitsspectrumforω0=0.86withandwithout a Hamming window.</li>
<li>Write a program that will take a 128 element vector known to contain cos (ω0t + δ ) forarbitraryδ and0.5&lt;ω0 &lt;1.5. Thevaluesoft gofrom−π toπ. Youhaveto extract the digital spectrum of the signal, find the two peaks at ±ω0, and estimate ω0 and δ.</li>
<li>Suppose the data in Q3 has added “white gaussian noise”. This can be generated by randn() in python. The extent of this noise is 0.1 in amplitude (i.e., 0.1*randn(N), where N is the number of samples). Repeat the problem and find the ω0 and δ
cos􏰆16􏰆1.5+ t 􏰇t􏰇 2π
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
5. Plot the DFT of the function

</div>
</div>
<div class="layoutArea">
<div class="column">
14

</div>
</div>
</div>
<div class="page" title="Page 15">
<div class="layoutArea">
<div class="column">
for t going from −π to π in 1024 steps. This is known as a “chirped” signal, and its frequency continuously changes from 16 to 32 radians per second. This also means that the period is 64 samples near −π and is 32 samples near +π.

6. For the same chirped signal, break the 1024 vector into pieces that are 64 samples wide. Extract the DFT of each and store as a column in a 2D array. Then plot the array as a surface plot to show how the frequency of the signal varies with time.

This is new. So far we worked either in time or in frequency. But this is a “time- frequency” plot, where we get localized DFTs and show how the spectrum evolves in time.

</div>
</div>
<div class="layoutArea">
<div class="column">
15

</div>
</div>
</div>
