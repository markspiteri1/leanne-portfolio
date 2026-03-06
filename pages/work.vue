<template>
  <div class="work-page">
    <div class="container mx-auto px-4 py-8">
      <div class="grid-layout">
        <!-- Sample images - replace these with actual artwork URLs -->
        <div class="grid-item">
          <img 
            src="https://images.unsplash.com/photo-1541961017774-22349e4a1262?w=400" 
            alt="Work 1" 
            class="artwork-image"
            @click="openImage($event)"
          />
        </div>
        
        <div class="grid-item">
          <img 
            src="https://images.unsplash.com/photo-1578662015715-58d0b71b97f0?w=400" 
            alt="Work 2" 
            class="artwork-image"
            @click="openImage($event)"
          />
        </div>
        
        <div class="grid-item">
          <img 
            src="https://images.unsplash.com/photo-1460661419201-fd4cecdf8a04?w=400" 
            alt="Work 3" 
            class="artwork-image"
            @click="openImage($event)"
          />
        </div>
        
        <div class="grid-item">
          <img 
            src="https://images.unsplash.com/photo-1513475382585-d06e58bcb0e0?w=400" 
            alt="Work 4" 
            class="artwork-image"
            @click="openImage($event)"
          />
        </div>
        
        <div class="grid-item">
          <img 
            src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?w=400" 
            alt="Work 5" 
            class="artwork-image"
            @click="openImage($event)"
          />
        </div>
        
        <div class="grid-item">
          <img 
            src="https://images.unsplash.com/photo-1547036967-23d11aacaee0?w=400" 
            alt="Work 6" 
            class="artwork-image"
            @click="openImage($event)"
          />
        </div>
        
        <div class="grid-item">
          <img 
            src="https://images.unsplash.com/photo-1578322450787-4d23bc4c4dca?w=400" 
            alt="Work 7" 
            class="artwork-image"
            @click="openImage($event)"
          />
        </div>
        
        <div class="grid-item">
          <img 
            src="https://images.unsplash.com/photo-1578322450794-ef70919adbf3?w=400" 
            alt="Work 8" 
            class="artwork-image"
            @click="openImage($event)"
          />
        </div>
      </div>
      
      <!-- Modal for full-size image view -->
      <div v-if="selectedImage" class="modal-overlay" @click="closeImage">
        <div class="modal-content" @click.stop>
          <button class="close-button" @click="closeImage">&times;</button>
          <img :src="selectedImage" :alt="selectedAlt" class="modal-image" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const selectedImage = ref(null);
const selectedAlt = ref('');

const openImage = (event) => {
  selectedImage.value = event.target.src;
  selectedAlt.value = event.target.alt;
};

const closeImage = () => {
  selectedImage.value = null;
  selectedAlt.value = '';
};

// Close modal on escape key
onMounted(() => {
  const handleEscape = (e) => {
    if (e.key === 'Escape') {
      closeImage();
    }
  };
  
  document.addEventListener('keydown', handleEscape);
  
  onUnmounted(() => {
    document.removeEventListener('keydown', handleEscape);
  });
});
</script>

<style scoped>
.work-page {
  min-height: 100vh;
  padding: 2rem 0;
}

.grid-layout {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1rem;
}

@media (min-width: 640px) {
  .grid-layout {
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  }
}

@media (min-width: 768px) {
  .grid-layout {
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  }
}

@media (min-width: 1024px) {
  .grid-layout {
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  }
}

.grid-item {
  overflow: hidden;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.grid-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
}

.artwork-image {
  width: 100%;
  height: auto;
  display: block;
  cursor: pointer;
  transition: transform 0.2s ease;
}

.artwork-image:hover {
  transform: scale(1.02);
}

/* Modal styles */
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.9);
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
}

.modal-content {
  position: relative;
  max-width: 90vw;
  max-height: 90vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal-image {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
  border-radius: 8px;
}

.close-button {
  position: absolute;
  top: -1rem;
  right: -1rem;
  background: white;
  border: none;
  border-radius: 50%;
  width: 2.5rem;
  height: 2.5rem;
  font-size: 1.5rem;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
  z-index: 1001;
}

.close-button:hover {
  background: #f3f4f6;
}
</style>