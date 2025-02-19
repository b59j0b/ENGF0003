java c
Ocean Acidification
ENGF0003 Coursework
24-25
Guidelines:
• Type your coursework in Word or LaTeX. Follow UCL Accessibility Guidelines to format your document. Include a table of contents, page numbers, and use built-in styles (Heading 1, Heading 2) to structure your document.
• All figures and tables must be numbered and contain informative captions. All the main equations throughout your work must be numbered and typed appropriately.
• Submit a single PDF document. Do not write down your name, student number, or any information that might help identify you in any part of the coursework. Do not copy and paste the coursework brief into your submission – Rewrite information where necessary for the sake of your argument.
This coursework counts towards 20% of your final ENGF0003 grade.
Context
The Great Barrier Reef (GBR) is a collective of over 2,900 individual reefs near the coast of Queensland in Australia. Selected as a World Heritage Site in 1981, the GBR is the largest structure composed of living organisms on the planet.
The GBR is a fundamental component of ocean health, supporting a wide diversity of marine life. However, it is estimated that the Reef has lost half of its corals over the last three decades due to ocean acidification and temperature variations.
What is Ocean Acidification?
When the oceans absorb excess carbon dioxide, chemical reactions increase the abundance of hydrogen ions, lowering the pH of the water and making it less alkaline. It is estimated that the oceans have absorbed about 23% of all CO2 emitted by human activities.
"For eons, the world's oceans have been sucking carbon dioxide out of the atmosphere and releasing it again in a steady inhale and exhale. The ocean takes up carbon dioxide through photosynthesis by plant-like organisms (phytoplankton), as well as by simple chemistry: carbon dioxide dissolves in water." (Holli Riebeek in an article for the NASA Earth Observatory, 2008)
The ocean's ability to absorb carbon is decreasing. MIT scientists found in a 2017 study that the amount of carbon absorbed by the ocean has decreased by 1.5% due to human-caused CO2 emissions.
• This decrease means an amount of CO2 equivalent to the UK's yearly emissions.
• This excess carbon dioxide remains in surface waters and is not absorbed by the deep ocean.
The issue here is a change in the planet's natural carbon cycle. An increase in the atmospheric temperature and concentration of carbon dioxide makes the ocean's surface supersaturated with CO2. The less alkaline surface ocean waters can absorb less atmospheric carbon, leading to additional atmospheric heating due to accumulated CO2.
• Current estimates are that the oceans have the lowest mean pH of surface seawater in the last 800,000 years.
• This change in the chemistry of ocean surface water affects the ability of corals to build skeletons and provide a habitat for marine life.
• Without reefs, these ecosystems collapse, and marine life is endangered.
• This has profound implications for marine biodiversity since 25 to 30% of all marine species depend on coral reefs at some point in their life cycle.
How can mathematics help us analyse this problem?
You will analyse a dataset sourced from the Australian National Mooring Network (ANMN). This dataset contains measurements of ocean surface temperature [°C], atmospheric pressure [kPa], and carbon dioxide content [ppm] for both air and seawater. This data has been collected daily from 24 March 2011 to 24 March 2021 at midday. The data collection site is shown in Figure 1.
To learn how to analyse the data, it is important to complete Statistics Onramp and Common Data Analysis Techniques. These self-paced courses will teach you how to do basic statistical analysis of data in MATLAB.

Figure 1. Site of data collection (23°27'29.9"S 151°55'35.8"E).
1. Visualise, Summarise  Communicate the Data
20 MARKS - 2 PAGE MAXIMUM
Your task is to summarise, visualise, and describe the dataset attached to this brief and communicate the main patterns in the data in a concise, accurate and accessible way.
1.1. Produce one table summarising key metrics and statistics in the dataset.
1.2. Provide one 代 写ENGF0003 Ocean Acidification 24-25Matlab
代做程序编程语言short paragraph (300 words or less) justifying why you have chosen to summarise the data in the way you did in 1.1.
1.3. Explain the main trends and patterns you can take from this summary of the data.
2. Model and Evaluate Linear Behaviours in the Data
30 MARKS - 3 PAGE MAXIMUM
Your task is to create mathematical models of the data. Calculate a linear regression of the temperature T [˚C], atmospheric y [ppm] and water x [ppm] concentrations of CO2 as a function of time t in days.
2.1. Explain what the coefficients of the linear regression mean and evaluate the quality of the regressions by calculating, contrasting and comparing the coefficient of determination R2for each model.
2.2. Produce figures containing scatterplots of pressure, temperature, atmospheric, and water concentrations of CO2 with respect to time. Plot your linear regressions over the scatterplots.
2.3. Use your linear regression to forecast the concentration of CO2 in the atmosphere in 2030, 2050, and 2100. What do you think the concentration of CO2 in the atmosphere will be like? Discuss your confidence in your predictions, as well as factors that could make it inaccurate.
3. Model and Evaluate Seasonal Patterns in the Data
30 MARKS - 3 PAGE MAXIMUM
Use the template code provided in this brief to model temperature T in ˚C as a function of time t in days. The template code calculates the parameters k1, k2, k3 and k4 that minimise the error between Equation 1 and the data provided.



3.1. Use your knowledge in trigonometric functions to explain what the parameters k1, k2, k3 and k4 mean, giving real-world or engineering examples and analogies.
3.2. Demonstrate that the formula for the root mean square (RMS) of a sinusoidal wave of amplitude A over one period τ in Equation 2 is:

Then, estimate the amplitude of seasonal variations k1 for Eq. 1 through applying Eq. 2 to the data.
3.3. Use your knowledge or research in trigonometric functions and the provided data to make initial guesses for k2, kl3 and k4 and justify them.
3.4. Use your initial guesses in the code provided and describe the process of finding the best approximation possible. Contrast and compare the error of this approximation to the error of the linear regression approximation for T obtained in Task 2.
Template code:Q3model = @(params, d) params(1) * sin(2 * pi * params(2) * d + params(3)) +params(4);%insert your initial guesses for initial parameters in this vector by replacingthe '_' elementsinitial_parameters = [_ , _, _, _];%insert your initial guesses for the lower bound of parameters in this vectorlower_bounds = [ _, _, _, _];%insert your initial guesses for the upper bound of parameters in this vectorupper_bounds = [_ , _, _, _];[fitParams, resnorm, residual, exitflag, output] = ...lsqcurvefit(Q3model, initialParams, d_, T, lower_bounds, upper_bounds);% Write code to access the 'fitParams' variable to find out the values fitted foreach parameter% Calculate the fitted modelT_fit = Q3model(fitParams, d_);% plot a comparison of the data and your resultsfigure;plot(d, T, 'b.', 'MarkerSize', 12); hold on;plot(d, T_fit, 'r-', 'LineWidth', 2);xlabel('x label');ylabel('y label');title('Plot title');legend('Legend entry 1', 'Legend entry 2');grid on;
4. Reflection of learning
20 MARKS - 1 PAGE MAXIMUM
Write a conclusions section for your coursework. Write paragraphs or use bullet points summarising the main ideas and take-aways from each section in terms of:
• What you have learned while doing each question. Contrast and compare your knowledge, skills and attitudes before your studies at UCL and after completing this Coursework.
• What your results and analysis tell you about the concentration of CO2 in the GBR. Use an argument based on your mathematical knowledge and work to communicate succinctly how you arrived at your conclusions.
• What are the implications of your results for the environment, society and the economy. Provide a reasoning of what is important to you in analysing sustainability problems. Make a statement about how engineering students should approach problems involving mathematics and sustainability.







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
