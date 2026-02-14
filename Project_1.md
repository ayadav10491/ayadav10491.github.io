---
layout: project
title: Embedded Deep Learning Semantic Segmentation
---

<div class="container" style="max-width: 1000px;">
    
    <!-- Hero / Objective -->
    <div class="glass" style="padding: 40px; margin-bottom: 40px; text-align: center; animation: fadeInUp 0.8s ease-out;">
        <h1 style="font-size: 2.5rem; margin-bottom: 20px; color: var(--text-deep-teal);">Embedded Deep Learning Semantic Segmentation</h1>
        <div class="tags" style="justify-content: center; margin-bottom: 30px;">
            <span class="tag" style="font-size: 0.9rem; padding: 6px 15px;">TensorFlow Lite</span>
            <span class="tag" style="font-size: 0.9rem; padding: 6px 15px;">Computer Vision</span>
            <span class="tag" style="font-size: 0.9rem; padding: 6px 15px;">Embedded Systems</span>
        </div>
        <p style="font-size: 1.2rem; line-height: 1.8; color: var(--text-dark-teal); max-width: 800px; margin: 0 auto;">
            Created a vision-based environment surveying application using deep learning, specifically optimized to run efficiently on resource-constrained embedded devices.
        </p>
    </div>

    <!-- Workflow -->
    <h2 style="text-align: center; margin-bottom: 30px; font-size: 1.8rem;">System Workflow</h2>
    <div class="glass" style="padding: 30px; margin-bottom: 60px; text-align: center; transition: transform 0.3s;">
        <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/workflow.JPG?raw=true" 
             alt="Workflow Diagram" 
             style="max-width: 90%; border-radius: 12px; box-shadow: 0 8px 30px rgba(0,0,0,0.1);">
    </div>

    <!-- Training Specs Grid -->
    <h2 style="text-align: center; margin-bottom: 30px; font-size: 1.8rem;">Training Specifications</h2>
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 25px; margin-bottom: 60px;">
        <div class="glass" style="padding: 25px; text-align: center; display: flex; flex-direction: column; align-items: center; justify-content: center;">
            <i class="fas fa-eye" style="font-size: 2.5rem; color: var(--accent-rust); margin-bottom: 15px;"></i>
            <h3 style="font-size: 1.1rem; margin-bottom: 5px;">Task</h3>
            <p style="font-weight: 600; color: var(--text-deep-teal);">Semantic Segmentation</p>
        </div>
        <div class="glass" style="padding: 25px; text-align: center; display: flex; flex-direction: column; align-items: center; justify-content: center;">
            <i class="fas fa-database" style="font-size: 2.5rem; color: var(--accent-rust); margin-bottom: 15px;"></i>
            <h3 style="font-size: 1.1rem; margin-bottom: 5px;">Dataset</h3>
            <p style="font-weight: 600; color: var(--text-deep-teal);">CamVid</p>
        </div>
        <div class="glass" style="padding: 25px; text-align: center; display: flex; flex-direction: column; align-items: center; justify-content: center;">
            <i class="fas fa-project-diagram" style="font-size: 2.5rem; color: var(--accent-rust); margin-bottom: 15px;"></i>
            <h3 style="font-size: 1.1rem; margin-bottom: 5px;">Architecture</h3>
            <p style="font-weight: 600; color: var(--text-deep-teal);">Encoder-Decoder<br><span style="font-size: 0.9rem; font-weight: 400;">(UNet, SegNet)</span></p>
        </div>
        <div class="glass" style="padding: 25px; text-align: center; display: flex; flex-direction: column; align-items: center; justify-content: center;">
            <i class="fas fa-microchip" style="font-size: 2.5rem; color: var(--accent-rust); margin-bottom: 15px;"></i>
            <h3 style="font-size: 1.1rem; margin-bottom: 5px;">Encoder</h3>
            <p style="font-weight: 600; color: var(--text-deep-teal);">MobileNetV2</p>
        </div>
    </div>

    <!-- Compression & Results Split -->
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 40px; margin-bottom: 60px;">
        
        <!-- Optimization -->
        <div>
            <h2 style="text-align: center; margin-bottom: 25px; font-size: 1.6rem;">Optimization Strategy</h2>
            <div class="glass" style="padding: 30px; height: 100%;">
                <div style="margin-bottom: 25px;">
                    <div style="display: flex; align-items: center; margin-bottom: 15px; padding: 10px; background: rgba(255,255,255,0.5); border-radius: 8px;">
                        <i class="fas fa-check-circle" style="color: var(--accent-rust); font-size: 1.2rem; margin-right: 15px;"></i>
                        <div>
                            <strong style="display: block; font-size: 0.9rem; color: var(--text-dark-teal);">Technique</strong>
                            <span style="font-size: 1.1rem; font-weight: 600;">Post-Training Quantization</span>
                        </div>
                    </div>
                    <div style="display: flex; align-items: center; padding: 10px; background: rgba(255,255,255,0.5); border-radius: 8px;">
                        <i class="fas fa-tools" style="color: var(--accent-rust); font-size: 1.2rem; margin-right: 15px;"></i>
                        <div>
                            <strong style="display: block; font-size: 0.9rem; color: var(--text-dark-teal);">Framework</strong>
                            <span style="font-size: 1.1rem; font-weight: 600;">TensorFlow Lite</span>
                        </div>
                    </div>
                </div>
                <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/comp_and_inf.png?raw=true" 
                     alt="Optimization Process" 
                     style="width: 100%; border-radius: 8px; box-shadow: 0 4px 15px rgba(0,0,0,0.05);">
            </div>
        </div>

        <!-- Metric Results -->
        <div>
           <h2 style="text-align: center; margin-bottom: 25px; font-size: 1.6rem;">Compression Results</h2>
           <div class="glass" style="padding: 30px; height: 100%; text-align: center; display: flex; flex-direction: column; justify-content: center;">
               <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/model_size.jpg?raw=true" 
                    alt="Model Size Comparison" 
                    style="max-width: 100%; border-radius: 10px; margin-bottom: 20px;">
               <p style="font-size: 1.1rem; font-weight: 500; color: var(--text-deep-teal);">
                   Achieved significant reduction in model size with minimal loss in accuracy.
               </p>
           </div>
        </div>
    </div>

    <!-- Live Inference Section -->
    <div style="margin-bottom: 60px;">
        <h2 style="text-align: center; margin-bottom: 30px; font-size: 1.8rem;">Live Inference using TFLite Interpreter</h2>
        <div class="glass" style="padding: 30px; text-align: center; max-width: 800px; margin: 0 auto;">
            <div style="position: relative; display: inline-block;">
                <img src="https://github.com/ayadav10491/Portfolio/blob/master/images/camvid.gif?raw=true" 
                     alt="Real-time Inference" 
                     style="max-width: 100%; border-radius: 12px; box-shadow: 0 10px 40px rgba(0,0,0,0.15);">
                <div style="margin-top: 20px; font-style: italic; color: var(--text-dark-teal);">
                    Real-time semantic segmentation running on embedded hardware
                </div>
            </div>
        </div>
    </div>

</div>
